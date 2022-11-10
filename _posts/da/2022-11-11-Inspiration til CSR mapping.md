---
layout: post
title:  "Inspiration til bæredygtigheds kortlægning"
date:   2022-11-10 17:11:00 +0100
permalink: news/invitation-til-CSR-mapping
tags: foodefficiency
ref: webinar

---


![Inspirations webinar](/assets/images/Invitation%20Inspiration%20.png)

**Kom godt i gang med bæredygtighedskortlægning – nemt, overskueligt og effektivt**

Begreberne fyger stadig om os – ESG, zero emission, grøn taxonomi, science based targeting, socialt ansvar, green washing og meget mere. 

Så hvad er op og ned - Og hvad giver mening af fokusere på når man som virksomhed står på en brændende platform med stigende priser på energi, transport, råvarer og mangel på arbejdskraft?

Hos ESG in Business vil vi gerne hjælpe med at gøre arbejdet med bæredygtighed nemt, overskueligt og effektivt.

På baggrund af over 25 års erfaring med klima og bæredygtighed i globale forsyningskæder, har vi udviklet et værktøj til kortlægning af små og mellemstore virksomheders bæredygtighedsindsats. 

Som inspiration til bæredygtighedsarbejdet vil vi gennemgå hovedpunkterne i værktøjet over en række webinarer – sammen med vores bedste tips og links til hvor du kan få mere viden til at skabe værdi på bundlinjen. 

For det er jo bundlinjen det handler om - den tre-delte bundlinje. People – Planet – Profit 

Webinarene er rettet mod virksomhedsejere såvel som produktions-, kvalitets- og salgschefer i små og mellemstore virksomheder.
Deltagelse er gratis men kræver tilmelding da der er begrænsning på 25 deltagere. Hvert webinar har en varighed af ca. 30 minutter.

Tilmelding sker via formularen nedenfor 



## Webinarserie - Inspiration til bæredygtighedskortlægning
{: #subject}

Jeg vil gerne tilmeldes følgende datoer:

<div class="contact-inner">
<div class="inquiries">
  <form accept-charset="UTF-8" class="new_inquiry" id="new_inquiry" method="post" data-name="Contact form">
    <div style="margin:0;padding:0;display:inline">
      <input id="locale" name="locale" type="hidden" value="da">
      <input id="utf8" name="utf8" type="hidden" value="✓">
      <input id="authenticity_token" name="authenticity_token" type="hidden" value="8vr2lMQljUu/67VhB2GS5pXRZubfGknz0sIweGYatWU=">
    </div>

    <div>
      <label class="checkbox field">
          <input type="checkbox" name="30/11-2022" checked />
          <span>
            Tirsdag den 30/11 kl. 8:30 – Klima, miljø og biodiversitet
        </span>
      </label>      
      <label class="checkbox field">
          <input type="checkbox" name="31/11-2022" checked />
          <span>
          Onsdag den 31/11 kl. 8:30 – Medarbejdere - Sikkerhed, trivsel og kompetencer
        </span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="1/12-2022" checked />
          <span>
          Torsdag den 1/12 kl. 8:30 - Indkøb – Varer, transport og serviceydelser
        </span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="2/12-2022" checked />
          <span>
           Fredag den 2/12 kl. 8:30 - Virksomhedsetik og samfundsansvar
        </span>
      </label>
    </div>

    <!-- <div class="field message_field">
      <label class="placeholder-fallback" for="inquiry_message">Besked *</label>
      <textarea cols="40" id="inquiry_message" name="message" placeholder="Specielle forhold vedr. tilmelding" rows="8"></textarea>
    </div> -->
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_name">Navn *</label>
      <input class="text" id="inquiry_name" name="name" placeholder="" required="required" size="30" type="text">
    </div>
    <input id="inquiry_info2" class="offscreen" name="inquiry_info2" tabindex="-1" type="text" value="">
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_email">Email *</label>
      <input class="text email" id="inquiry_email" name="email" placeholder="" required="required" size="30" type="email">
    </div>
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_phone">Telefon</label>
      <input class="text phone" id="inquiry_phone" name="phone" placeholder="" size="30" type="phone">
    </div>
    <div class="actions">
      <input class="btn btn-success" id="contact_submit" name="commit" type="submit" value="Send tilmelding">
    </div>
  </form>
</div>
</div>
<script type="text/javascript">
function clearInquiryForm() {
  // document.getElementById("inquiry_message").value = "";
  document.getElementById("inquiry_name").value = "";
  document.getElementById("inquiry_email").value = "";
  document.getElementById("inquiry_phone").value = "";
}

// ContactUs API
document.getElementById("contact_submit").addEventListener("click", function(event){
  event.preventDefault()

  const locale = document.getElementById("locale").value;
  const checkedBoxes = document.querySelectorAll('input[type=checkbox]:checked');
  var message = "Tilmelding til følgende events:\n";
  checkedBoxes.forEach(input => {
      message = message + " *  " + input.name + "\n";
    });
  const name = document.getElementById("inquiry_name").value;
  const info2 = document.getElementById("inquiry_info2").value;
  const email = document.getElementById("inquiry_email").value; 
  const phone = document.getElementById("inquiry_phone").value; 
  const subject = "[ESG] " + document.getElementById("subject").innerText;
  const data = { locale, subject, message, name, info2, email, phone }
  const url = 'https://fb65cne4o6.execute-api.eu-central-1.amazonaws.com/send';
  const headers = {
    'Access-Control-Allow-Origin': '*',
    'Access-Control-Allow-Credentials': true,
  }
  axios.post(url, data, headers).then(res => {
    alert('Mange tak for din tilmelding.  Vi vil vende tilbage snarest muligt.');
    clearInquiryForm();
  }).catch(err => {
    console.log(err)
    alert("Der skete en fejl. Check om du har udfyldt felterne: besked, navn, email og telefon samt om du har netforbindelse.\n\nFejltekst: " + err);
  })
  return true;
});
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/axios/0.18.0/axios.min.js"></script>

Opstår der problemer med tilmelding så brug venligst vores kontaktformular eller send en email til info@foodefficiency.eu
