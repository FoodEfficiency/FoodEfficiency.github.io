---
layout: post
title:  "Invitation til webinarserie om klima og bæredygtighed - Myter og Muligheder"
date:   2023-01-02 07:11:00 +0100
permalink: news/invitation-til-webinarserie-om-klima-og-baeredygtighed
tags: foodefficiency
ref: webinar
redirect_from:
  - news/invitation-til-webinarserie-om-klima-og-bæredygtighed
---


<img width="1424" alt="Screenshot 2021-10-15 at 07 59 06" src="https://user-images.githubusercontent.com/75361000/137440046-f11da098-5d02-40c5-8ccd-7fe4b6fe4b64.png">

Klima og den grønne dagsorden giver din virksomhed eller organisation mulighed for at differentiere sig både på det lokale og det globale marked. 

Klimadagsordenen er nemlig ikke kun et benspænd. Der stilles nye og foranderlige krav til din virksomhed om at efterleve omverdens krav og forventninger til bæredygtighed. Dine kunder og investorer forventer, at I arbejder med øget fokus på grøn omstilling, bæredygtighed og samfundsansvar.

**ESG in Business**  har 25 års erfaring i at navigere i klima- og bæredygtighedsdagsordenen. Vi får hurtigt øje på potentialer, og vi kan hjælpe din virksomhed med kortlægning og identifikation af fokusområder til at understøtte klimaet og bæredygtig udvikling på tværs af organisationen. I kan nemlig bygge videre på jeres eksisterende fundament og sikre forankring og værdiskabelse på tværs af organisationen under hensyntagen til bæredygtighedsprincipperne. 

Vi udbyder derfor en serie af fire webinars, hvor Jeres virksomhed kan blive klogere på bæredygtighed, under følgende overskrifter;

 **1. Introduktion til bæredygtighed - myter og muligheder**
 
 **2. Klima og bæredygtighed – direkte og indirekte påvirkninger (scope 1, 2 og 3)**
 
 **3. Bæredygtighedsfokus med udgangspunkt i dansk lovgivning og ledelsessystemer**
 
 **4. Kommunikation af bæredygtighed (intern og eksterne)**


Webinarene er rettet mod virksomhedsejere såvel som produktions-, kvalitets- og salgschefer i små og mellemstore virksomheder.

Deltagelse er gratis, der er plads til max 12  deltagere. Hvert webinar har en varighed af ca. 30 minutter med efterfølgende 15 min til spørgsmål og uddybende kommentarer.

Tilmelding sker via formularen nedenfor.

### Webinarserie om klima og bæredygtighed
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
          <input type="checkbox" name="20/1-2023" checked />
          <span>Fredag den 20/1 kl 8:30 - Introduktion til bæredygtighed - myter og muligheder</span>
      </label>      
      <label class="checkbox field">
          <input type="checkbox" name="27/1-2023" checked />
          <span>Fredag den 27/1 kl 8:30 - Klima og bæredygtighed – direkte og indirekte påvirkninger</span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="3/2-2023" checked />
          <span>Fredag den 3/2 kl 8:30 - Bæredygtighedsfokus med udgangspunkt i lovgivning og ledelsessystemer</span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="10/2-2023" checked />
          <span>Fredag den 10/2 kl 8:30 - Kommunikation af bæredygtighed (intern og eksterne)</span>
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
