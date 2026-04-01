# Husky Sips — Hillcrest High School Business Club

A custom dirty soda ordering page for Husky Sips at Hillcrest High School. Students can browse the signature menu, build their own drink, submit an order tray, and get a receipt.

---

## How to Customize

### 1. Hero Background Photo (Line 57)
**Location:** Look for the `.hero-card` class in the `<style>` section.

**Action:** Replace the URL inside `url("...")` with your new school or background photo link.

**Note:** This is a CSS background, so keep the `linear-gradient(...)` part in front of the URL so the text stays readable over the photo.

---

### 2. Changing the Featured Drink (Line 564)
**Location:** Near the top of the `<script>` tag. Look for `var featuredIndex = 9;`.

**Action:** Change the number to any value between 0 and 12 to instantly swap the drink shown at the top of the page.

| Index | Drink Name        | Base      |
|-------|-------------------|-----------|
| 0     | Texan             | Dr Pepper |
| 1     | The OG            | Dr Pepper |
| 2     | Ms Peachy         | Dr Pepper |
| 3     | Bleed Green       | Dr Pepper |
| 4     | Harvey's Secret   | Dr Pepper |
| 5     | The McCann        | Coke      |
| 6     | Beachy            | Coke      |
| 7     | Peaches and Limes | Coke      |
| 8     | Shark Bite        | Sprite    |
| 9     | Hula Harvey       | Sprite    |
| 10    | High Tide         | Sprite    |
| 11    | Watermelon Rush   | Sprite    |
| 12    | Dawg Pound        | Sprite    |

---

### 3. Editing Drink Details & Photos (Lines 544–558)
**Location:** Inside the `var drinks = [...]` array in the `<script>` tag.

**Action:** You can update the `name`, `desc` (description), `note`, `tag`, or `img` (photo URL) for any of the 13 signature drinks.

**Example:** To change the Bleed Green photo, find the line starting with `{ name: "Bleed Green"` and replace the URL in the `img:` field.

---

### 4. Gallery Photos (Lines 501, 505, 509)
**Location:** Inside the `<section id="gallery">` area.

**Action:** Find the `style="background-image:url('...')"` attribute on each of the three gallery cards and replace the URL with your new photo.

---

### 5. Request Form Link (Line 520)
**Location:** Inside the `<section id="request">` area.

**Action:** Find the `<a>` tag and replace the `href="https://forms.gle/..."` URL with your new Google Form link.

---

### 6. School Hours & Info (Lines 531–534)
**Location:** Inside the `<section id="hours">` area (and also the small info cards on lines 371–373).

**Action:** Update the text inside the `<p>` tags if the open days or peak time ever changes. Currently set to **Tue & Wed**, **2nd Period**.
