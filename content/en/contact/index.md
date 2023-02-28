---
title: "Contact"
description: "Drop us an email."
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
  background: #d0dfe8;
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
  border-bottom: 4px solid #3e4f24;
  background: #5a7233; 
  font-size: 16px;
  font-weight: 400;
  color: #fff;
  }
  .green-button:hover {
  background: #3e4f24;
  }
</style>

<form name="contact" method="POST" data-netlify="true">
  <div class="form-inner">
    <p>
      <label>Your Name: <input type="text" name="name" /></label>
    </p>
    <p>
      <label>Your Email: <input type="email" name="email" /></label>
    </p>
    <p>
      <label>Message: <textarea name="message" rows="5"></textarea></label>
    </p>
    <p>
      <button class="green-button" type="submit">Submit</button>
    </p>
  </div>
</form>
