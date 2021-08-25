---
layout: post
title:  "Invitation til webinarserie om klima og bæredygtighed"
date:   2021-08-26 09:11:00 +0100
tags: foodefficiency
ref: webinar
---

<img width="909" alt="Screenshot 2021-08-24 at 15 17 09" src="https://user-images.githubusercontent.com/75361000/130623686-7719b258-53a2-401b-89b0-0a0fa133193e.png">

Klima og den grønne dagsorden er ikke blot en udfordring men også en mulighed for at din virksomhed eller organisation kan differentiere sig på det lokale såvel som globale marked. 

Det stiller nye og foranderlige krav til virksomheder om at efterleve omverdens krav samt forventninger til bæredygtighed. Samtidig forventer kunderne at virksomheden arbejder med øget fokus på grøn omstilling, bæredygtighed og samfundsansvar.

De færreste virksomheder starter dog på bar bund men har allerede implementeret initiativer og processer som understøtter FN’s verdensmål. Dette med udgangspunkt i lovkrav, krav fra ledelsessystemer samt teknologi og best practice. 
Det er derfor vigtigt at bygge videre på det eksisterende fundament og sikre forankring og værdiskabelse på tværs af organisationen, under hensyntagen til bæredygtighedsprincipperne.  
FoodEfficiency kan hjælpe din virksomhed med kortlægning og identifikation af fokusområder der understøtter klimaet og bæredygtig udvikling på tværs af organisationen.

Vi udbyder derfor en serie af fire webinars, hvor Jeres virksomhed kan blive klogere på bæredygtighed, under følgende overskrifter;

1.	Introduktion til bæredygtighed og værdiskabelse 
2.	Klima og bæredygtighed – direkte og indirekte påvirkninger (scope 1, 2 og 3)
3.	Bæredygtighedsfokus med udgangspunkt i dansk lovgivning og ledelsessystemer 
4.	Kommunikation af bæredygtighed (intern og eksterne)


Webinarene er rettet mod ejere såvel som produktions-, kvalitets- og salgschefer i små og mellemstore virksomheder, der interesserer sig hvordan bæredygtighed kan være med til skabe værdi for organisationen.

Webinarene er gratis og har hver en varighed af ca. 30 minutter med efterfølgende 15 min til spørgsmål og uddybende kommentarer. 

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
          <input type="checkbox" name="24/09-2021" checked />
          <span>Fredag den 24/9 kl 9:30</span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="01/10-2021" checked />
          <span>Fredag den 1/10 kl 9:30</span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="08/10-2021" checked />
          <span>Fredag den 8/10 kl 9:30</span>
      </label>
      <label class="checkbox field">
          <input type="checkbox" name="15/10-2021" checked />
          <span>Fredag den 15/10 kl 9:30</span>
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
    alert('Mange tak for din tilmelding.  Vi vil vende tilbage snarest muligt.');
    clearInquiryForm();
  }).catch(err => {
    console.log(err)
    alert("Der skete en fejl. Check om du har udfyldt felterne: besked, navn, email og telefon");
  })
  return true;
});
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/axios/0.18.0/axios.min.js"></script>
