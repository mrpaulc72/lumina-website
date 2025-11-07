# Contact Form Setup Guide

Your website now has a beautiful contact form, but it needs a quick 5-minute setup to start receiving messages.

---

## ✅ What You Get

- Name, email, phone, and message fields
- Spam protection included
- Email notifications to **shaferk18@gmail.com**
- Works alongside the Calendly booking widget
- Mobile-responsive design
- Free for up to 50 submissions/month

---

## 🚀 Quick Setup (5 minutes)

### Step 1: Create Free Formspree Account

1. Go to **https://formspree.io/register**
2. Sign up with email (can use shaferk18@gmail.com)
3. Verify your email address

### Step 2: Create New Form

1. After logging in, click **"+ New Form"**
2. **Name**: `Lumina Contact Form`
3. **Email**: `shaferk18@gmail.com` (where messages will be sent)
4. Click **"Create Form"**

### Step 3: Get Your Form ID

After creating the form, you'll see an endpoint like:
```
https://formspree.io/f/xblrwkyz
```

Copy the part after `/f/` (example: `xblrwkyz`)

### Step 4: Update Website

Open `index.html` and find this line (around line 692):

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="space-y-6">
```

Replace `YOUR_FORM_ID` with your actual form ID:

```html
<form action="https://formspree.io/f/xblrwkyz" method="POST" class="space-y-6">
```

### Step 5: Push to GitHub

```bash
cd /Users/paul/dev/lumina-website
git add index.html
git commit -m "Connect contact form to Formspree"
git push
```

---

## ✨ Done!

- Test by submitting the form on your website
- You'll receive an email at **shaferk18@gmail.com**
- The first submission requires you to confirm your email (one-time only)

---

## 📊 Formspree Dashboard

Login anytime to:
- View all form submissions
- Download submission data
- Configure spam filters
- Set up auto-responses
- Add custom thank-you messages

**Dashboard**: https://formspree.io/forms

---

## 🎨 Current Layout

Your contact section now has:

1. **Calendly Widget** (primary option - instant booking)
2. **"OR"** divider
3. **Contact Form** (alternative - for general inquiries)

This gives visitors flexibility while prioritizing the consultation booking.

---

## 🆓 Free Tier Limits

- 50 submissions/month (free)
- If you need more, upgrade plans start at $10/month
- You'll get email alerts at 80% and 100% usage

---

## 🔧 Optional Customizations

### Add Custom Thank You Message

In Formspree dashboard:
1. Go to your form settings
2. Under "Options" → "Redirect"
3. Add: `https://mrpaulc72.github.io/lumina-website/?submitted=true`

Then we can show a custom thank you message on the page.

### Add Auto-Response

In Formspree dashboard:
1. Go to form settings
2. Enable "Auto-responder"
3. Customize the message sent to people who submit the form

---

## Need Help?

If you run into any issues during setup, just let me know!

