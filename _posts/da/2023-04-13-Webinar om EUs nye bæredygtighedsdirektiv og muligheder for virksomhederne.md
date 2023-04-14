layout: post
title:  "Invitation til webinar om EUs nye bæredygtighedsdirektiv - for de virksomheder der IKKE er DIREKTE omfattet af direktivet"
date:   2023-04-13 07:11:00 +0100
permalink: news/invitation-til-webinar-om-EUs-nye-bæredygtighedsdirektiv
tags: foodefficiency
ref: webinar CSRD og ESRS
---
**Webinar om EUs nye bæredygtighedsdirektiv og muligheder**
![00 CSR](https://user-images.githubusercontent.com/75361000/229443419-00831445-fdb4-4849-bb31-38ef09519ced.jpg#pull-right;w360)

Det nye europæiske bæredygtighedsdirektiv (CSRD) er trådt I kraft – men faktisk forvente Erhvervsstyrelsen at blot 2300 danske virksomheder at blive direkte omfattet.

Men mange virksomheder bliver indirekte omfattet eftersom de skal levere bæredygtighedsdata til deres kunder for de varer og services som leveres. 

Det drejer sig bl.a. om rapportering indenfor klima, forurening og biodiversitet, medarbejder og ansættelsesforhold samt produkt og forbrugeransvar. 
Det er nemlig nogle af de emner der skal rapporteres på under de nye europæiske bæredygtigheds rapporterings standarder (ESRS).

Men den øgede data indsamling og rapportering kan også give værdi for din virksomhed – og det kan hjælpe dig at værdisætte bæredygtighed på dine varer og ydelser, som du aktivt kan bruge i forhandlingerne med dine kunder.

Vil du høre mere så tilmeld dig vores webinar som giver dig overblik over de nye krav og de muligheder som kommer i kølvandet på EU’s nye rapporteringskrav.

På webinaret hører du om følgende emner;
- Introduktion til til CSRD – hvem er omfattet 
- Introduktion til ESRS – hovedpunkter 
- Kom godt i gang med rapportering 
  -	Ved brug af eksisterende standarder
  -	Ved indledende kortlægning 
- Sæt pris på din bæredygtighed 


Webinarene er rettet mod virksomhedsejere såvel som økonomi- og salgschefer i små og mellemstore virksomheder.

Deltagelse er gratis og har en varighed af ca 30 minuter samt 15 minuter til debat. Der er plads til max 12  deltagere pr event, og der udbydes tre datoer.

### Webinar om EUs nye bæredygtighedsdirektiv og muligheder for virksomhederne
{: #subject}

Jeg vil gerne tilmeldes webinaret på følgende dato:

<div class="contact-inner">
<div class="inquiries">
  <form accept-charset="UTF-8" class="new_inquiry" id="new_inquiry" method="post" data-name="Contact form">
    <div style="margin:0;padding:0;display:inline">
      <input id="locale" name="locale" type="hidden" value="da">
      <input id="utf8" name="utf8" type="hidden" value="✓">
      <input id="authenticity_token" name="authenticity_token" type="hidden" value="8vr2lMQljUu/67VhB2GS5pXRZubfGknz0sIweGYatWU=">
    </div>

    <div>
      <fieldset>
        <label class="radio field">
          <input type="radio" name="event_date" value="12/5-2023" />
          <span>Fredag den 12/5 kl 8:30 </span>
        </label>      
        <label class="radio field">
          <input type="radio" name="event_date" value="26/5-2023" />
          <span>Fredag den 26/5 kl 8:30 </span>
        </label>
        <label class="radio field">
          <input type="radio" name="event_date" value="2/6-2023" />
          <span>Fredag den 2/6 kl 8:30 </span>
        </label>
      </fieldset>
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
  const checkedRadios = document.querySelectorAll('input[type=radio]:checked');
  var message = "Tilmelding til følgende event(s):\n";
  checkedBoxes.forEach(input => {
      // var nextSibling = input.nextSibling;
      // while(nextSibling && nextSibling.nodeType != 1) {
      //   nextSibling = nextSibling.nextSibling
      // }
      // message = message + " *  " + nextSibling.innerHTML + " - " + input.value || input.name + "\n";
      message = message + " *  " + input.name + "\n";
    });
  checkedRadios.forEach(input => {
      message = message + " *  " + input.value + "\n";
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
