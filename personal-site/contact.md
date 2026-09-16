---
layout: default
title: Contact
permalink: /contact/
---
<div class="single-column page">
  <h1>Contact</h1>
  <p>Want to work together, or just say hi? Fill out the form below.</p>

  {% if site.formspree_id and site.formspree_id != "" %}
  <form action="https://formspree.io/f/{{ site.formspree_id }}" method="POST" class="contact-form">
    <label for="name">Name</label>
    <input type="text" id="name" name="name" required>

    <label for="email">Email</label>
    <input type="email" id="email" name="_replyto" required>

    <label for="message">Message</label>
    <textarea id="message" name="message" rows="6" required></textarea>

    <button type="submit">Send message</button>
  </form>
  {% else %}
  <p><em>Set <code>formspree_id</code> in <code>_config.yml</code> to enable this form (sign up free at
  <a href="https://formspree.io" target="_blank" rel="noopener">formspree.io</a>), or replace this block with a
  mailto link: <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>.</em></p>
  {% endif %}
</div>
