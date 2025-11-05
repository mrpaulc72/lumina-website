# Content Replacement Guide
## Lumina Property Management Homepage

This guide provides specific instructions for replacing placeholder content before launch.

---

## Critical Replacements (Must Complete Before Launch)

### 1. Hero Section Background Image

**Current Location**: Line 115 in `index.html`

**Current Code**:
```html
<section class="min-h-screen flex items-center justify-center relative" style="background: linear-gradient(rgba(42, 42, 42, 0.4), rgba(42, 42, 42, 0.4)), url('https://images.unsplash.com/photo-1600210492493-0946911123ea?q=80&w=2074&auto=format&fit=crop') center/cover no-repeat;">
```

**What You Need**:
- High-resolution luxury property interior photo (minimum 1920px x 1080px)
- Shows a bright, airy, minimalist living space (the RESULT, not workers)
- Embodies "Japandi" or modern Scandinavian luxury aesthetic
- Professional quality with natural light

**How to Replace**:
1. Save your image as `hero-image.jpg` in an `/assets/images/` folder
2. Replace the URL in line 115:
```html
style="background: linear-gradient(rgba(42, 42, 42, 0.4), rgba(42, 42, 42, 0.4)), url('/assets/images/hero-image.jpg') center/cover no-repeat;"
```

**Optimization Tips**:
- Compress image to <500KB for fast loading (use tinypng.com)
- Save as JPG for photographs
- Test load speed after replacement

---

### 2. Solution Section Image

**Current Location**: Line 271 in `index.html`

**Current Code**:
```html
<img src="https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?q=80&w=2053&auto=format&fit=crop" 
     alt="Luxury property interior" 
     class="w-full h-96 object-cover">
```

**What You Need**:
- Another high-quality luxury property image
- Different from hero (shows variety of your properties)
- Serene, spa-like bedroom or architectural detail preferred
- Shows meticulous care and attention to detail

**How to Replace**:
1. Save as `solution-image.jpg` in `/assets/images/`
2. Replace in line 271:
```html
<img src="/assets/images/solution-image.jpg" 
     alt="Meticulously maintained luxury property interior" 
     class="w-full h-96 object-cover">
```

---

### 3. Contact Form Integration

**Current Location**: Lines 488-524 in `index.html`

**Current Status**: Static HTML form (doesn't send anywhere)

**Integration Options**:

#### Option A: Netlify Forms (Easiest if hosting on Netlify)
Add `netlify` attribute to form tag:
```html
<form class="space-y-4 text-left" netlify name="consultation">
```

#### Option B: Formspree
1. Create account at formspree.io
2. Create new form, get endpoint URL
3. Update form action:
```html
<form action="https://formspree.io/f/YOUR-FORM-ID" method="POST" class="space-y-4 text-left">
```

#### Option C: Direct Email Integration
1. Set up server-side form handler
2. Add action and method to form tag
3. Configure email notifications

#### Option D: CRM Integration (HubSpot, Salesforce, etc.)
1. Get form embed code from your CRM
2. Replace entire form section with CRM form
3. Style to match brand (may require custom CSS)

**Required After Integration**:
- [ ] Test form submission
- [ ] Verify email notification received
- [ ] Check form data captured correctly
- [ ] Set up auto-responder (optional but recommended)

---

### 4. Service Area Specification

**Current Location**: Line 461 in `index.html` (FAQ Question 4)

**Current Text** (Too vague):
```html
<p class="text-lg leading-relaxed">
    We currently serve exclusive properties in select luxury markets. Contact us to discuss your property's location 
    and how we can serve you.
</p>
```

**Replace With** (Specific):
```html
<p class="text-lg leading-relaxed">
    We currently serve exclusive properties in [YOUR ACTUAL MARKETS: e.g., "Lake Tahoe, Aspen, and Scottsdale"]. 
    We're expanding to additional luxury markets in 2025. Contact us to discuss your property's location and how we can serve you.
</p>
```

---

## Recommended Replacements (When Available)

### 5. Testimonials

**Current Status**: Using monogram circles (SC, MD, JA) - This looks professional and protects privacy

**If You Have Real Testimonials**:

**Option A**: Keep monograms, update quotes and attribution
- Lines 295-320 (Testimonial 1)
- Lines 323-348 (Testimonial 2)
- Lines 351-376 (Testimonial 3)

**Option B**: Add actual photos
Replace monogram div with image:
```html
<!-- Current -->
<div class="monogram">SC</div>

<!-- Replace with -->
<img src="/assets/images/testimonial-1.jpg" 
     alt="S. Chen" 
     class="w-20 h-20 rounded-full mx-auto mb-4 object-cover">
```

**Best Practice**: Only use real photos with explicit permission

---

### 6. "Featured In" Logos

**Current Location**: Lines 378-382 in `index.html`

**Current Status**: Text only

**If You Have Actual Features**:
Add logo images:
```html
<div class="text-center mt-16 pt-12 border-t border-antique-gold">
    <p class="text-sm uppercase tracking-widest mb-6">As Featured In</p>
    <div class="flex justify-center items-center gap-8 flex-wrap">
        <img src="/assets/images/logo-luxury-portfolio.png" 
             alt="Luxury Portfolio International" 
             class="h-12 opacity-80 hover:opacity-100 transition">
        <img src="/assets/images/logo-forbes.png" 
             alt="Forbes Global Properties" 
             class="h-12 opacity-80 hover:opacity-100 transition">
    </div>
</div>
```

---

## Optional Enhancements (Future)

### 7. Additional Property Images

**Potential Locations**:
- After "Three Quick Outcomes" section (add visual break)
- Before "Final Call-to-Action" (reinforce quality)

**Suggested Addition** (after line 221):
```html
<!-- Optional: Property Showcase -->
<section class="py-16">
    <div class="container mx-auto max-w-6xl">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <img src="/assets/images/property-1.jpg" 
                 alt="Luxury property" 
                 class="w-full h-96 object-cover rounded-sm">
            <img src="/assets/images/property-2.jpg" 
                 alt="Luxury property" 
                 class="w-full h-96 object-cover rounded-sm">
        </div>
    </div>
</section>
```

---

### 8. Favicon & Social Sharing Images

**Favicon**:
Add in `<head>` section (around line 10):
```html
<link rel="icon" type="image/png" href="/assets/images/favicon.png">
<link rel="apple-touch-icon" href="/assets/images/apple-touch-icon.png">
```

**Open Graph (Social Sharing)**:
Add in `<head>` section:
```html
<!-- Open Graph / Facebook -->
<meta property="og:type" content="website">
<meta property="og:title" content="Lumina Property Management - Where Transparency Meets Luxury">
<meta property="og:description" content="Redefining luxury property management with unparalleled service and complete, real-time transparency for discerning property owners.">
<meta property="og:image" content="https://yourdomain.com/assets/images/og-image.jpg">

<!-- Twitter -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Lumina Property Management - Where Transparency Meets Luxury">
<meta name="twitter:description" content="Redefining luxury property management with unparalleled service and complete transparency.">
<meta name="twitter:image" content="https://yourdomain.com/assets/images/og-image.jpg">
```

**OG Image Requirements**:
- Size: 1200px x 630px
- Shows brand identity clearly
- Includes logo and tagline
- Looks good in preview

---

## Image Sourcing Guidelines

### If You Don't Have Professional Photography Yet

**Temporary High-Quality Placeholder Sources**:
1. **Unsplash.com** (free, high-quality)
   - Search: "luxury interior," "modern luxury home," "minimalist living room"
   - Download highest resolution
   - Attribute if required by license

2. **Pexels.com** (free, no attribution required)
   - Similar search terms
   - Verify commercial use allowed

3. **Shutterstock/Adobe Stock** (paid, professional)
   - More specific luxury property options
   - Licensed for commercial use
   - Higher quality selection

**Photography Style Guide** (for hiring photographer):
- Bright, airy, natural light
- Minimalist Japandi aesthetic
- No people visible
- Focus on space and quality materials
- Serene, spa-like feel
- Clean lines and uncluttered spaces

---

## Quality Checklist

Before considering any replacement "done," verify:

### For Images
- [ ] High resolution (at least 1920px wide for hero, 1200px for others)
- [ ] Properly compressed (<500KB for large images, <200KB for smaller)
- [ ] Appropriate file format (JPG for photos, PNG for logos/graphics)
- [ ] Matches brand aesthetic (airy, luxurious, minimalist)
- [ ] Shows RESULTS not process (no workers, equipment, offices)
- [ ] Alt text added for accessibility
- [ ] Tested on mobile devices

### For Contact Form
- [ ] Submission successfully sends
- [ ] Email notification received
- [ ] All data captured correctly
- [ ] Auto-responder works (if configured)
- [ ] Thank you message displays
- [ ] Tested from multiple devices
- [ ] Spam protection enabled (if applicable)

### For Text Content
- [ ] No placeholder text remains (e.g., "YOUR MARKETS HERE")
- [ ] All contact information accurate
- [ ] Service areas clearly specified
- [ ] Grammar and spelling verified
- [ ] Tone matches brand voice (sophisticated, positive, confident)
- [ ] No Lorem Ipsum or dummy text

---

## Replacement Timeline

### Day 1: Critical Path
1. Contact form integration (2-3 hours)
2. Hero image replacement (30 minutes)
3. Test form submission (15 minutes)
4. Service area text update (10 minutes)

### Day 2: Quality Content
1. Solution section image (30 minutes)
2. Optimize all images (<500KB each) (1 hour)
3. Test on mobile devices (30 minutes)
4. Final proofread of all text (30 minutes)

### Day 3: Polish
1. Add favicon and OG images (1 hour)
2. Review testimonials (if updating) (1 hour)
3. Add featured logos (if available) (30 minutes)
4. Final quality check (1 hour)

---

## File Organization

**Recommended Structure**:
```
/lumina-website/
├── index.html
├── README.md
├── EXECUTIVE_SUMMARY.md
├── QUICK_START.md
├── CONTENT_REPLACEMENT_GUIDE.md (this file)
├── lumina-website-and-brand
└── /assets/
    └── /images/
        ├── hero-image.jpg
        ├── solution-image.jpg
        ├── testimonial-1.jpg (optional)
        ├── testimonial-2.jpg (optional)
        ├── testimonial-3.jpg (optional)
        ├── logo-luxury-portfolio.png (optional)
        ├── logo-forbes.png (optional)
        ├── favicon.png
        ├── apple-touch-icon.png
        └── og-image.jpg
```

---

## Support & Questions

### If Images Don't Display
1. Check file path is correct (case-sensitive)
2. Verify images are in correct folder
3. Clear browser cache and refresh
4. Check browser console for errors

### If Form Doesn't Work
1. Verify form action/method is correct
2. Check all required fields have `required` attribute
3. Test with different email addresses
4. Check spam folder for notifications
5. Verify integration credentials are correct

### If Content Looks Wrong
1. Check HTML tags are properly closed
2. Verify no accidental deletions of critical code
3. Test in multiple browsers
4. Clear cache before testing changes

---

## Final Pre-Launch Checklist

Once all replacements are complete:

- [ ] All placeholder images replaced
- [ ] Contact form working and tested
- [ ] Service areas specified
- [ ] All text proofread (no placeholders)
- [ ] Images optimized for web (<500KB)
- [ ] Mobile display verified
- [ ] All links functional
- [ ] Browser testing completed (Chrome, Firefox, Safari, Edge)
- [ ] Page load time <3 seconds
- [ ] Analytics installed and tracking
- [ ] Favicon displays correctly
- [ ] Social sharing images set up

**When all checkboxes are complete, you're ready to launch!**

---

**Need Help?** Reference README.md for technical details or QUICK_START.md for launch process.

