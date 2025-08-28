# 🎉 Birthday Card –(HTML/CSS/JS)

> 📌 Repo: `BIRTHAY-CARD-`

---

## ✨ Features

* One‑page birthday card (no build tools required)
* Multilingual greeting: easily switch or cycle through many languages
* Personalized name & message
* Confetti/animation option
* Responsive layout (mobile & desktop)
* Dark-friendly color palette

---

## 🚀 Quick Start

1. **Clone or Download** this repository.

   ```bash
   git clone https://github.com/BOURZGUIHIBA/BIRTHAY-CARD-.git
   ```
2. Open `index.html` directly in your browser (double-click) or use a simple local server:


## 🛠️ Customize

### 1) Change the Name

* Open `index.html` (or `app.js` if the logic is separated).
* Find the variable or element for the **recipient name** and replace it.

### 2) Change the Message

* Update the main message text (e.g., a short wish).

### 3) Colors & Fonts

* Edit `styles.css` to tweak primary colors, gradients, and fonts.
* Tip: keep good contrast for readability.

### 4) Turn On/Off Confetti

* If a `confetti` or `particles` function exists in `app.js`, set it to `true/false`.

---

## 🌍 Multilingual Setup

Add or edit translations in `app.js` (or `translations.js`), for example:

```js
const greetings = [
  { lang: 'Français', text: 'Joyeux Anniversaire' },
  { lang: 'English',  text: 'Happy Birthday' },
  { lang: 'العربية',  text: 'عيد ميلاد سعيد' },
  { lang: 'Türkçe',   text: 'Doğum Günün Kutlu Olsun' },
  { lang: 'Español',  text: 'Feliz Cumpleaños' },
  // add as many as you like…
];
```

Then render the current greeting (example):

```js
let i = 0;
function showNextGreeting() {
  const g = greetings[i % greetings.length];
  document.querySelector('#greeting').textContent = g.text;
  document.querySelector('#lang').textContent = g.lang;
  i++;
}
setInterval(showNextGreeting, 2000);
showNextGreeting();
```

> You can pin a **default language** by putting it first in the array.

---

## 📁 Project Structure (suggested)

```
BIRTHAY-CARD-/
├─ index.html
├─ styles.css
├─ app.js
├─ assets/
│  ├─ preview.png (optional)
│  └─ confetti.min.js (optional)
└─ README.md
```

---

## 🧪 Testing Checklist

* Text shows birthday greetings in your languages.
* Works on **mobile** (small screens) and desktop.
* Fonts load correctly.
* No overlapping animations; performance is smooth.

---

## ♿ Accessibility Tips

* Use **semantic** HTML (`<main>`, `<h1>`, buttons with labels).
* Provide **aria-labels** for decorative controls.
* Keep **color contrast** ≥ 4.5:1 for text.
* Avoid flashing effects faster than 3/s.

---

## 📸 Preview

Add a screenshot at `assets/preview.png` and display it in `index.html` or here in the README:

```md
![Birthday Card Preview](assets/preview.png)
```

---

## 🤝 Contributing

PRs to improve styles, add languages, or fix typos are welcome. Please keep the project **simple** (no heavy frameworks).

---

## 🧾 License

This project is licensed under the MIT License. You are free to use, modify, and share.
