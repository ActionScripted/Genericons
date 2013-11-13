Genericons Provisions
===

Genericons are vector icons embedded in a webfont designed to be clean and simple keeping with a generic aesthetic and were originall created by Automattic (http://genericons.com/ and https://github.com/Automattic/Genericons). Use genericons for instant HiDPI, to change icon colors on the fly, or even with CSS effects such as drop-shadows or gradients!

Genericons are awesome but their development is a bit cautious (rightfully so). Genericons Provisions aims to contribute new glyphs and offer ways for developers to deploy their own versions or contribute to existing ones using provided source files in a more expedient manner.


Feedback
---

If you have any needs, changes, suggestions or just want to drop a line please [submit an issue](https://github.com/ActionScripted/Genericons/issues).


Contributing
---

Currently only setup to work with Glyphs (http://glyphsapp.com/) but will hopefully be providing the source files in other formats (Fontlab, FontForge, etc.) or settle on a single format...eventually.

New glyphs:

    * Grab the free version of Glyphs
    * Drop your new glyphs in, being mindful of the code point numbering for type groups (social, etc.)
    * Submit a pull request


Contribution Notes
---
    * Use advanced mode in FontSquirrel or you're going to get a subset of glyphs and things won't work
    * For rapid glyph development, you can start in Illustrator (2800x2800) and copy/paste into Glyphs


Usage
---

To use, place the font folder in your stylesheet directory and paste this in your CSS file:

    /* =Genericons, thanks to FontSquirrel.com for conversion!
    -------------------------------------------------------------- */
    @font-face {
        font-family: 'genericons-reloadedregular';
        src: url('genericons-reloaded-regular-webfont.eot');
        src: url('genericons-reloaded-regular-webfont.eot?#iefix') format('embedded-opentype'),
            url('genericons-reloaded-regular-webfont.woff') format('woff'),
            url('genericons-reloaded-regular-webfont.ttf') format('truetype'),
            url('genericons-reloaded-regular-webfont.svg#genericons-reloadedregular') format('svg');
        font-weight: normal;
        font-style: normal;
    }

Note: the above only works if you don't use a CDN. If you do, or don't know what that is, you should use the syntax that's embedded in genericons.css.

From then on, you can create an icon like this:

    .my-icon:before {
        content: '\f101';
        display: inline-block;
        font: normal 16px/1 'Genericons-Provisions';
        vertical-align: top;
        -webkit-font-smoothing: antialiased;
    }

This will output a comment icon before every element with the class "my-icon". The "content: '\f101';" part of this CSS is easily copied from the helper tool at http://genericons.com/

You can also use the bundled example.css if you'd rather insert the icons using HTML tags.


Notes
---

Photoshop mockups:

Genericons-Regular.otf found in the root directory of this zip has not been web-font-ified. So you can drop it in your system fonts folder and use the font in Photoshop if you like.

For those of you using Genericons in your Photoshop mockup, remember to delete the old version of the font from Font Book, and grab the new one from the zip file. This also affects using it in your webdesigns: if you have an old version of the font installed locally, that's the font that'll be used in your website as well, so if you're missing icons, check for old versions of the font on your system.

Pixel grid:

Note that Genericons has been designed for a 16x16 pixel grid. That means it'll look sharp at font-size: 16px exactly. It'll also be crisp at multiples thereof, such as 32px or 64px. It'll also look reasonably crisp at in-between font sizes such as 24px or 48px, but not quite as crisp as 16 or 32. Please don't set the font-size to 17px, though, that'll just look terrible.

Also note the CSS property "-webkit-font-smoothing: antialiased". That makes the icons look great in WebKit browsers. Please see http://noscope.com/2012/font-smoothing for more info.


Change Log
---

V3.0.3:
Forked, readme changes, Trip Advisor, source files and a few other bits
    * Forked from https://github.com/Automattic/Genericons
    * Converted README to Markdown and updated a bit
    * Added Trip Advisor to the end of the logos/social/sharing range at code point (\F299)
    * Adding Glyphs file (http://www.glyphsapp.com/)
    * Adding release tag for downloads


Pre-Fork Change Log (from https://github.com/Automattic/Genericons)
---

V3.0.2:
A slew of new stuff and updates.
    * Social icons: Skype, Digg, Reddit, Stumbleupon, Pocket.
    * New generic icons: heart, lock and print.
    * New editing icons: code, bold, italic, image
    * New interaction icons: subscribe, unsubscribe, subscribed, reply all, reply, flag.
    * The hyperlink icon has been updated to be clearer, chunkier.
    * The "home" icon has been updated for style, size and clarity.
    * The email icon has been updated for style and clarity, and to fit with the new subscribe icons.
    * The document icon has been updated for style.
    * The "pin" icon has been updated for style and clarity.
    * The Twitter icon has been scaled down to fit with the other social icons.

V3.0.1:
Mostly maintenance.
    * Fixed an issue with the example page that showed an old "top" icon instead of the actual NEW "refresh" icon.
    * Added inverse Google+ and Path.
    * Replaced tabs with spaces in the helper CSS.
    * Changed the Genericons.com copy/paste tool to serve span's instead of div's for casual icon insertion. It's being converted to "inline-block" anyway.

V3.0:
Mainly maintenance and a few new icons.
    * Fast forward, rewind, PollDaddy, Notice, Info, Help, Portfolio
    * Updated the feed icon. It's a bit smaller now for consistency, the previous one was rather big.
    * So, the previous version numbering, 2.09, wasn't very PHP version compare friendly. So from now on it'll be 3.0, 3.1 etc. Props Ipstenu.
    * Genericons.com now has a mini release blog.
    * The CSS has prettier formatting, props Konstantin Obenland.

V2.09:
Updated Facebook icon to new version. Updated Instagram logo to use new one-color version. Updated Google+ icon to use same radius as Instagram and Facebook. Added a bunch of new icons, cog, unapprove, cart, media player buttons, tablet, send to tablet.

V2.06:
Included Base64 encoded version. This is necessary for Genericons to work with CDNs in Firefox. Firefox blocks fonts linked from a different domain. A CDN (typically s.example.com) usually puts the font on a subdomain, and is hence blocked in Firefox.

V2.05:
Added a bunch of new icons, including upload to cloud, download to cloud, many more.

V2:
Initial public release
