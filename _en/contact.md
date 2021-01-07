---
title: Contact
<!-- permalink: /contact/ -->
menu: foodefficiency
index: 2
ref: contact
---

# Contact us

<div class="contact-inner">
<div class="pull-right w50">
  <h3 class="brand">Food<span>Efficiency</span></h3>
  <p>Chr. M. Østergaards Vej 4a<br>DK-8700 Horsens</p>
  <p>Tel: +45 2987 8494</p>
  <p>CVR: 34428832</p>
  <p>Get in touch with us. Just fill in the form below and we'll get back to you as soon as we can.</p>
</div>
<div class="inquiries pull-left">
  <form accept-charset="UTF-8" action="/contact" class="new_inquiry" id="new_inquiry" method="post">
    <input id="locale" name="locale" type="hidden" value="da">
    <input id="utf8" name="utf8" type="hidden" value="✓">
    <input id="authenticity_token" name="authenticity_token" type="hidden" value="8vr2lMQljUu/67VhB2GS5pXRZubfGknz0sIweGYatWU=">
    <div class="field message_field">
      <label class="placeholder-fallback" for="inquiry_message">Message *</label>
      <textarea cols="40" id="inquiry_message" name="message" placeholder="Write your inquiry here" required="required" rows="8"></textarea>
    </div>
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_name">Name *</label>
      <input class="text" id="inquiry_name" name="name" placeholder="" required="required" size="30" type="text">
    </div>
    <input id="lastname" class="offscreen" name="lastname" type="text" value="">
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_email">Email *</label>
      <input class="text email" id="inquiry_email" name="email" placeholder="" required="required" size="30" type="email">
    </div>
    <div class="field">
      <label class="placeholder-fallback" for="inquiry_phone">Phone</label>
      <input class="text phone" id="inquiry_phone" name="phone" placeholder="" size="30" type="phone">
    </div>
    <div class="actions">
      <input class="btn btn-success" id="contact_submit" name="commit" type="submit" value="Send message">
    </div>
  </form>
</div>
</div>
<script type="text/javascript">
 // ContactUs API
document.getElementById("contact_submit").addEventListener("click", function(event){
  event.preventDefault()

  const locale = document.getElementById("locale").value;
  const message = document.getElementById("inquiry_message").value;
  const name = document.getElementById("inquiry_name").value;
  const lastname = document.getElementById("lastname").value;
  const email = document.getElementById("inquiry_email").value; 
  const phone = document.getElementById("inquiry_phone").value; 
  const data = { locale, message, name, lastname, email, phone }
  const url = 'https://fb65cne4o6.execute-api.eu-central-1.amazonaws.com/send';
  const headers = {
    'Access-Control-Allow-Origin': '*',
    'Access-Control-Allow-Credentials': true,
  }
  axios.post(url, data, headers).then(res => {
    alert("Thanks for your inquiry.  We'll get back to you as soon as we can.")
  }).catch(err => {
    console.log(err)
    alert(err)
  })
  return true;
});
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/axios/0.18.0/axios.min.js"></script>
