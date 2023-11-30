---
title: "Contact"
description: "Contact Us."
date: 2020-08-27T19:25:12+02:00
lastmod: 2020-08-27T19:25:12+02:00
draft: false
images: []
---

<script src="https://www.google.com/recaptcha/api.js" async defer></script>
<style>
  .form-inner {
  padding: 40px;
  }
  .form-inner input,
  .form-inner textarea {
  display: block;
  width: 100%;
  padding: 15px;
  margin-bottom: 10px;
  border: none;
  border-radius: 20px;
  background: #dff5e5;
  }
  .form-inner textarea {
  resize: none;
  }
  .green-button {
  width: 100%;
  padding: 10px;
  margin-top: 20px;
  border-radius: 20px;
  border: none;
  background: #15ba47;
  font-size: 16px;
  font-weight: 400;
  color: #fff;
  }
  .green-button:hover {
  background: #00581b;
  }
  .hidden {
  display: none;
  }
</style>

<form name="contact" method="POST" data-netlify="true" data-netlify-recaptcha="true">
  <div class="form-inner">
      <p>Your Name: </p>
      <input type="text" name="name" />
      <p>Your Email: </p>
      <input type="email" name="email" />
      <p>Message: </p>
      <textarea name="message" rows="5"></textarea>
      <div
        class="g-recaptcha"
        data-sitekey="6Lf9GcYkAAAAAJQx-4juYVGuVZZWIcjEio64gclx"
        data-callback="callback"
      ></div>
      <p style="color: red" id="warnMessage">You need to solve the CAPTCHA before you can submit the form.</p>
      <button class="green-button hidden" type="submit" id="btnSubmit">Submit</button>
  </div>
</form>
<script type="text/javascript">
  function callback() {
    const submitButton = document.getElementById("btnSubmit");
    const warnMessage = document.getElementById("warnMessage");
    submitButton.classList.remove("hidden");
    warnMessage.classList.add("hidden");
  }
</script>

<div class="text-center">
  <p>You can also chat with us on Discord:</p>
  <p>
    <a href="https://chat.virtualhub.eu.org">
      <img src="https://discordapp.com/api/guilds/1176107431013646357/widget.png?style=banner2" alt="Discord Banner"/>
    </a>
  <p>
</div>
