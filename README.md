Markdown
🥤 Husky Sips POS Web App
Hillcrest High School 

---

## 🌟 Overview
Husky Sips is a single-page application (SPA) that allows baristas and customers to:
* Browse a curated signature menu.
* Build custom soda combinations with real-time price calculation.
* Generate a digital, timestamped receipt for order verification.
* Capture orders via a mobile-friendly "Screenshot" mode.

---

## 🕹️ User Operations

### Creating an Order
1. **Signature Drinks:** Click any item in the "Menu" or "Favorites" section to add it directly to the tray.
2. **Custom Drinks (BYO):** - Select **one** Soda Base (required).
   - Select any number of **Add-ons** (syrups/creams).
   - Click **Add to Tray**.
3. **Reviewing:** Click the 🛒 **Order Tray** in the header to view items, remove mistakes, or clear the order.

### Checkout Process
1. Open the Order Tray and click **Generate Receipt**.
2. A receipt modal will appear with a unique timestamp.
3. The customer should show this screen to the barista for drink preparation and payment.
4. Click **Screenshot** to save a copy to the device gallery.

---

## 🛠️ Developer Guide

### 📍 Key File Structure
* **CSS Variables (`:root`):** Manage the brand colors (Greens and Creams) and border radiuses.
* **JavaScript Arrays:** Manage the actual "data" of the shop.

### 💵 Editing Prices
To update costs, locate the following variables in the `<script>` section:

| Variable | Description |
| :--- | :--- |
| `basePrice` | The starting cost for a "Build Your Own" soda. |
| `addonPrice` | The cost added for every flavor chip selected. |
| `menuItems` | An array of objects where you can change `price` for signature drinks. |

### 🍹 Adding New Menu Items
Add a new object to the `menuItems` array in the script:
```javascript
{ id: 6, name: "New Drink Name", price: 3.50, desc: "Ingredients list" }
Then, add the corresponding HTML button in the Menu Layout section:

HTML
<div class="item" onclick="addToTray(6)"> ... </div>
🧊 Adding New Flavors (Add-ons)
Simply add a string to the addons array. The UI will automatically generate a new clickable "chip" for that flavor:

JavaScript
const addons = ["Vanilla", "Coconut", "Strawberry", "Peach"];
⚙️ Customization Logic
The app uses a state-based logic to prevent errors:

Validation: The "Add Custom Drink" button is disabled until a currentBase is selected.

Math: Total Price = basePrice + (selectedAddons.length * addonPrice).

Persistence: This app is volatile. Refreshing the browser will clear the current tray. This is intentional to prevent order carry-over between different customers.

🆘 Troubleshooting
Q: The images aren't loading!

A: Ensure the device is connected to the internet. If the school's firewall blocks the image hosting domain, update the url() links in the CSS to point to local files.

Q: The "Add to Tray" button is unresponsive.

A: Ensure a Base Soda is highlighted. The app requires a base before it can calculate a custom drink.

Q: The Receipt is showing the wrong time.

A: The receipt uses the device's system time. Ensure the tablet or phone is set to the correct local time zone.

📝 License & Credits
Developed for the Hillcrest High School Business.
developed by michael bennett. (and fixed by ai)
