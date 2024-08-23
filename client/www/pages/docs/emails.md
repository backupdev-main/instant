---
title: Custom email templates and senders
---

You can customize all aspects of your Instant app's "magic code" email: the body (plain text or HTML), subject, sender name, and even the `from` address.

Set up custom magic code emails in the [Dashboard Auth tab](https://instantdb.com/dash?s=main&t=auth).

## Variables

We provide a handful of variables you can use in both your subject line and body template. Using a variable is as easy as adding the target's name in curly brackets, e.g. `{variable_name}`.

```html
<p>Hi {user_email}, here's your code for {app_title}:</p>

<strong>{code}</strong>
```

Here are the variables we offer:

- `{code}`, the magic code, e.g. _123456_. Note, this variable is required in both the subject and body.
- `{user_email}`, the recipient user's email address, e.g. *happyuser@gmail.com*
- `{app_title}`, your app's name

## Custom sender addresses

You can also set Instant's email's `from` and `reply-to` fields to an address on your own domain.

If you provide a custom sender address, you'll need to confirm it before we can start delivering from it. Our email partner, Postmark, will send a confirmation to the provided address with a link to verify. Until the address is verified, emails will continue to be sent from Instant's default auth sender (`auth@pm.instantdb.com`).