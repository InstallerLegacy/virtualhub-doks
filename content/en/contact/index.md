---
title: "Contact"
description: "Contact Us."
date: 2020-08-27T19:25:12+02:00
lastmod: 2020-08-27T19:25:12+02:00
draft: false
images: []
---

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
</style>

<form name="contact" method="POST" data-netlify="true">
  <div class="form-inner">
      <p>Your Name: </p>
      <input type="text" name="name" />
      <p>Your Email: </p>
      <input type="email" name="email" />
      <p>Message: </p>
      <textarea name="message" rows="5"></textarea>
      <button class="green-button" type="submit">Submit</button>
  </div>
</form>
