---
title: Contact
<!-- permalink: /en/contact/ -->
menu: foodefficiency
index: 3
ref: contact
---

# Contact us

<div class="contact-inner">
<div class="pull-right w50">
  <h3 class="brand">Food<span>Efficiency</span></h3>
  <p>Jessensgade 1, 3. sal<br>DK-8700 Horsens</p>
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
    <input id="inquiry_info2" class="offscreen" name="inquiry_info2" tabindex="-1" type="text" value="">
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
function clearInquiryForm() {
  document.getElementById("inquiry_message").value = "";
  document.getElementById("inquiry_name").value = "";
  document.getElementById("inquiry_email").value = "";
  document.getElementById("inquiry_phone").value = "";
}

// ContactUs API
document.getElementById("contact_submit").addEventListener("click", function(event){
  event.preventDefault()

  const locale = document.getElementById("locale").value;
  const message = document.getElementById("inquiry_message").value;
  const name = document.getElementById("inquiry_name").value;
  const info2 = document.getElementById("inquiry_info2").value;
  const email = document.getElementById("inquiry_email").value; 
  const phone = document.getElementById("inquiry_phone").value; 
  const data = { locale, message, name, info2, email, phone }
  const url = 'https://fb65cne4o6.execute-api.eu-central-1.amazonaws.com/send';
  const headers = {
    'Access-Control-Allow-Origin': '*',
    'Access-Control-Allow-Credentials': true,
  }
  axios.post(url, data, headers).then(res => {
    alert("Thanks for your inquiry.  We'll get back to you as soon as we can.");
    clearInquiryForm();
  }).catch(err => {
    console.log(err)
    alert("Could not submit yor contact request. Please specify inquiry parameters: message, name, email and phone");
  })
  return true;
});
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/axios/0.18.0/axios.min.js"></script>
