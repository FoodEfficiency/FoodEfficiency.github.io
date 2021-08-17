---
title: Test tilmeldingsformular
ref: tilmelding
---

# <span id="subject">test-tilmelding til Gaa-hjem-møde</span>

...(fra tidligere event side)...
FoodEfficiency afholder jævnligt gratis gå-hjem-møder og webinars for små og mellemstore virksomheder under temaet er **Få bæredygtighed ned på jorden og ind i hverdagen**.  

Møderne afholdes i de udviklingsparker i Jylland hvor FoodEfficiency har adgang til mødefaciliteter. 

## Planlagte møder/webinars i vinteren 2020/21:

* 16\. december - Vitus Bering Innovation Park, Chr. M. Østergaards Vej 4a, 8700 Horsens - også som webinar
* 19\. januar - Vitus Bering Innovation Park, Chr. M. Østergaards Vej 4a, 8700 Horsens - også som webinar 

Alle møderne afholdes kl 15:00-16:30.

Møderne er gratis at deltage i og tilmelding sker på [keh@foodefficiency.eu ][3] Ved tilmelding bedes du angive om du ønsker fysisk deltagelse eller via webinar. Grundet ønsket om mulig dialog er deltagerantal begrænse til 12 virksomheder (20 deltager) og max. 5 til fysisk deltagelse. 

## Tilmeldingsformular

Jeg vil gerne tilmeldes følgende datoer:

<div class="contact-inner">
<div class="inquiries pull-left">
  <form accept-charset="UTF-8" class="new_inquiry" id="new_inquiry" method="post" data-name="Contact form">
    <div style="margin:0;padding:0;display:inline">
      <input id="locale" name="locale" type="hidden" value="da">
      <input id="utf8" name="utf8" type="hidden" value="✓">
      <input id="authenticity_token" name="authenticity_token" type="hidden" value="8vr2lMQljUu/67VhB2GS5pXRZubfGknz0sIweGYatWU=">
    </div>
    <div>
      <label class="checkbox field">
          <input type="checkbox" name="09/09-2021" checked />
          <span>Torsdag den 9. september 19:00-21:30</span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="25/09-2021" checked />
          <span>Lørdag 25. september 15:00-19:00</span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="26/09-2021" checked />
          <span>Søndag 26. september 07:00-10:00</span>
      </label>
    </div>
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_name">Navn *</label>
      <input class="text" id="inquiry_name" name="name" placeholder="" required="required" size="30" type="text">
    </div>
    <input id="lastname" class="offscreen" name="lastname" tabindex="-1" type="text" value="">
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_email">Email *</label>
      <input class="text email" id="inquiry_email" name="email" placeholder="" required="required" size="30" type="email">
    </div>
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_phone">Telefon</label>
      <input class="text phone" id="inquiry_phone" name="phone" placeholder="" size="30" type="phone">
    </div>
    <div class="actions">
      <input class="btn btn-success" id="contact_submit" name="commit" type="submit" value="Send besked">
    </div>
  </form>
</div>
</div>
<script type="text/javascript">
function clearInquiryForm() {
  // document.getElementById("inquiry_message").value = "";
  // document.getElementById("inquiry_name").value = "";
  // document.getElementById("inquiry_email").value = "";
  // document.getElementById("inquiry_phone").value = "";
}
// function getChechedCheckboxes() {
//   var checkboxes = document.getElementsByName(chkboxName);
//   var checkboxesChecked = [];
//   // loop over them all
//   for (var i=0; i<checkboxes.length; i++) {
//      // And stick the checked ones onto an array...
//      if (checkboxes[i].checked) {
//         checkboxesChecked.push(checkboxes[i]);
//      }
//   }
//   // Return the array if it is non-empty, or null
//   return checkboxesChecked.length > 0 ? checkboxesChecked : null;
// }

// ContactUs API
document.getElementById("contact_submit").addEventListener("click", function(event){
  event.preventDefault()

  const locale = document.getElementById("locale").value;
  const checkedBoxes = document.querySelectorAll('input[type=checkbox]:checked');
  var message = "Tilmelding til følgende events:\n";
  checkedBoxes
    .forEach((input) => {
      message = message + " *  " + input.name + "\n";
    });
  const subject = document.getElementById("subject").innerText;
  const name = document.getElementById("inquiry_name").value;
  const lastname = document.getElementById("lastname").value;
  const email = document.getElementById("inquiry_email").value; 
  const phone = document.getElementById("inquiry_phone").value; 
  const data = { locale, message, subject, name, lastname, email, phone }
  const url = 'https://fb65cne4o6.execute-api.eu-central-1.amazonaws.com/send';
  const headers = {
    'Access-Control-Allow-Origin': '*',
    'Access-Control-Allow-Credentials': true,
  }
  axios.post(url, data, headers).then(res => {
    alert('Mange tak for din henvendelse.  Vi vil vende tilbage snarest muligt.');
    clearInquiryForm();
  }).catch(err => {
    console.log(err)
    alert("Der skete en fejl. Check om du har udfyldt felterne: besked, navn, email og telefon");
  })
  return true;
});
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/axios/0.18.0/axios.min.js"></script>
