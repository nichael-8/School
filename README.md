1. Hero Background Photo (Line 50)
Location: Look for the .hero-card class in the <style> section.

Action: Replace the URL inside url("...") with your new school or background photo link.

Note: This is a CSS background, so ensure you keep the linear-gradient part if you want the text to remain readable over the photo.

2. Changing the Featured Drink (Line 233)
Location: Scroll to the very bottom of the script. Look for let featuredIndex = 3;.

Action: Change the number to any value between 0 and 12 to instantly swap the drink shown at the top of the page.

0 = Texan, 3 = Bleed Green, 8 = Shark Bite, etc.

3. Editing Drink Details & Photos (Lines 207–230)
Location: Inside the const drinks = [...] array in the <script> tag.

Action: You can update the name, desc (description), note, tag, or img (photo URL) for any of the 13 signature drinks.

Example: To change the Bleed Green photo, find the line starting with { name: "Bleed Green" and replace the URL in the img: field.

4. Gallery Photos (Lines 149, 153, 157)
Location: Inside the <section id="gallery"> area.

Action: Find the style="background-image:url('...')" attribute for each of the three gallery cards and replace the URL with your new photo path.

5. Request Form Link (Line 167)
Location: Inside the <section id="request"> area.

Action: Find the <a> tag and replace the href="https://forms.gle/..." URL with your new Google Form link.

Note: There is also a link in the top navigation bar at Line 101 that you should update to match.

6. School Hours & Info (Lines 179–181)
Location: Inside the <section id="hours"> area.

Action: Update the text inside the <p> tags if the "Open Days" or "Peak Time" ever changes.