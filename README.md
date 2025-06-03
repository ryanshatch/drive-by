# Tor Mirror & Archives – Drive-By Dropper

## Overview

This landing page is designed to **automatically serve a malicious ZIP payload** when a visitor opens the site. It leverages a browser’s automatic download capabilities using JavaScript, ideal for quick drive-by distribution on the open web, Tor hidden services, or onion mirrors.

---

## Setup Instructions

1. **Project Structure**  
   - Place `index.html` at the root of your hosting directory.
   - Put your payload ZIP file (`MrSuicide.zip`) inside `/assets/` (create the folder if needed).
   - The file path can be changed in the script comment if you rotate payloads.

2. **HTML Breakdown**
   - When the page loads, the script triggers `downloadZip()` automatically.
   - The script:
     - Issues an HTTP GET for `/assets/MrSuicide.zip`
     - Receives it as a binary blob
     - Creates a temporary link
     - Simulates a user click to force the browser to download the file
     - Cleans up any traces from the DOM for stealth

3. **Customization**
   - Edit the `<title>` and `<h1>` in `index.html` to match your operation, e.g., rebrand for music leaks, darknet drops, or file vaults.
   - Update the ZIP filename or folder structure if your server has different routing.

4. **Deployment**
   - Deploy to any host that allows custom HTML/JS (Cloudflare Pages, GitHub Pages, static S3 bucket, Tor hidden service, etc.)
   - **Note:** Some browsers block auto-downloads without user interaction; optimal results on less-secure browsers or with tailored phishing lures.

5. **Stealth Notes**
   - Code cleans up the temporary download link after execution.
   - No user interaction is required for the download to trigger, but fallback to a manual download button if you need to support all browsers.

---

## Example Structure

```plaintext
.
├── assets
│   └── MrSuicide.zip
└── index.html
```

---

## Legal Note

For research or educational use only. You are responsible for compliance with laws and ethical guidelines in your jurisdiction.
## Disclaimer
This code is provided for educational and research purposes only. The author does not condone or support any illegal activities, including unauthorized distribution of software or malware. Use this code responsibly and in compliance with all applicable laws and regulations. Wherever you deploy this code, ensure it is done in a legal and ethical manner. The author is not liable for any misuse or consequences arising from the use of this code. In other words, do not use this code for malicious purposes or to harm others. Always respect the rights and privacy of individuals and organizations. And if you do use it, make sure you have permission to do so and that it is in line with ethical standards.
> <br>
> 
> **CRITICAL WARNING JUST FOR YOU: *NOT MY CHAIR NOT MY PROBLEM.*** <br><code>IF YOU USE THIS CODE, YOU ARE RESPONSIBLE FOR YOUR OWN ACTIONS. I AM NOT LIABLE FOR ANY FUCKERY THAT HAPPENS AS A RESULT OF USING THIS CODE. AGAIN. USE AT YOUR OWN RISK AND BY EVEN READING THIS YOU ARE WAVING ALL LEGAL AND ETHICAL TIES SO DO NOT BLAME ME WHEN YOU FUCK AROUND AND FIND OUT, GET CAUGHT, OR IF SOMETHING ELSE GOES WRONG.</code>
>
> **CRITICAL NOTE JUST FOR YOU ALSO:** I AM JUST THE MESSENGER, NOT THE MESSAGE.<br> RESPECTFULLY, PLEASE KINDLY DO NOT FUCKING SHOOT THE MESSENGER.<br> with that said here is your personally tailored disclaimer.<hr>
> <code>
> DONT BE A FUCKIN CLOWN! :clown: Use this at your own risk and Ill triple down that if you fucked around and found out, please kindly don't bitch and cry when the feds come knocking on your:
> <ul>
>   <li>tent</li>
>   <li>bando</li>
>   <li>mommas house</li>
>   <li>mommas basement</li>
>   <li>your girlfriend’s "safe spot"</li>
>   <li>your boyfriend’s "safe spot"</li>
>   <li>your best friend's "safe spot"</li>
>   <li>your other girlfriend’s "safe spot"</li>
>   <li>your other boyfriend’s baby mommas best friends auntie's "safe spot"</li>
>   <li>that stash house your weird uncle lets you borrow for when you "are sick" but really you just want to get high</li>
>   <li>grandma’s attic</li>
>   <li>your cousin’s trap house</li>
>   <li>the Dollar General parking lot</li>
>   <li>the local Waffle House booth</li>
>   <li>your baby mama’s porch</li>
>   <li>that one sketchy storage unit</li>
>   <li>the back seat of your ’07 Civic</li>
>   <li>your plug’s house</li>
>   <li>your buddy’s gamer den / mommas basement</li>
>   <li>the WiFi spot at the public library</li>
>   <li>behind the dumpster at Taco Bell</li>
>   <li>the abandoned Blockbuster</li>
>   <li>your "super secret anonymous" Discord server</li>
> </ul>
> ...or anywhere else you thought was off the radar. </code>
> <br><br>
<hr>
<h3>
FINAL WARNING — THIS IS ON YOU!<br><br>
If your eyes even touch this message, you’ve already surrendered every legal and moral excuse. Don’t come crying when the wolves are at your door, the badge is at your bando, or the feds are pounding on any spot you thought was safe. There are no do-overs, no mercy, and no one to blame but yourself.
</h3>