#Tailwind
---

## 📌 1. What is Tailwind CSS?

* Tailwind is a **utility-first** CSS framework.
* It allows you to style elements directly in HTML using **predefined utility classes**.
* Instead of writing custom CSS, you compose utility classes.
* Tailwind helps create **responsive**, **clean**, and **maintainable** UIs quickly.

---

## ⚙️ 2. Installation Methods

### 📦 Option 1: CDN (Quick use for demos)

```html
<script src="https://cdn.tailwindcss.com"></script>
```

### 💻 Option 2: Using CLI (Preferred)

```bash
npm install -D tailwindcss
npx tailwindcss init
```

### 📄 Create CSS input file

```css
/* input.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 🧾 Setup config file

```js
// tailwind.config.js
module.exports = {
  content: ["./*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### 🚀 Compile CSS

```bash
npx tailwindcss -i ./input.css -o ./dist/output.css --watch
```

---

## 🎨 3. Core Utility Classes

### 📐 Spacing (Margin & Padding)

```html
m-4         // margin: 1rem;
p-2         // padding: 0.5rem;
mt-3, mb-1  // margin-top: 0.75rem, margin-bottom: 0.25rem
px-4        // padding-left & right
py-2        // padding-top & bottom
```

### 📏 Sizing

```html
w-1/2       // width: 50%;
h-96        // height: 24rem;
min-w-full  // min-width: 100%;
max-h-screen
```

### 🌈 Colors

```html
text-blue-600      // text color
bg-red-400         // background color
border-green-300   // border color
hover:bg-yellow-500
```

---

## 🧱 4. Layout Utilities

### 🧭 Positioning

```html
static, relative, absolute, fixed, sticky
top-0, bottom-4, left-8, right-1/2
z-0, z-10, z-50
```

### 📐 Display

```html
block, inline-block, inline, hidden, flex, grid
```

### 📌 Object Fit & Position

```html
object-cover, object-contain
object-center, object-left
```

---

## 🧰 5. Flexbox Utilities

```html
flex, flex-row, flex-col
items-center, items-end
justify-center, justify-between, justify-evenly
gap-2, gap-x-4, gap-y-6
flex-wrap, flex-nowrap
```

---

## 🟦 6. Grid Utilities

```html
grid, grid-cols-2, grid-cols-4
col-span-2, row-span-3
gap-4, gap-x-2, gap-y-3
```

---

## ✏️ 7. Typography

```html
text-xs, text-sm, text-lg, text-2xl, text-6xl
font-light, font-normal, font-bold, font-extrabold
uppercase, lowercase, capitalize
tracking-tight, tracking-wider
leading-snug, leading-relaxed
```

---

## 🧱 8. Borders & Radius

```html
border, border-2, border-t, border-l-4
rounded, rounded-sm, rounded-md, rounded-full
border-dashed, border-solid, border-double
```

---

## 🎨 9. Background Utilities

```html
bg-gradient-to-r from-blue-400 to-purple-600
bg-no-repeat, bg-cover, bg-center, bg-fixed
```

---

## 🔁 10. Responsive Design

### 🔸 Breakpoints

* `sm` → 640px
* `md` → 768px
* `lg` → 1024px
* `xl` → 1280px
* `2xl` → 1536px

### 🔸 Usage

```html
<p class="text-sm md:text-xl lg:text-2xl">Responsive Text</p>
```

---

## 🌙 11. Dark Mode

```js
// In config
darkMode: "class"
```

```html
<div class="bg-white text-black dark:bg-gray-800 dark:text-white">
  Dark mode ready
</div>
```

---

## 💡 12. State Variants

```html
hover:bg-blue-700
focus:outline-none
active:scale-95
disabled:opacity-50
group-hover:text-red-400
```

---

## 🧩 13. Plugins

### 🔌 Common Plugins

```bash
npm install @tailwindcss/forms @tailwindcss/typography
```

```js
plugins: [
  require('@tailwindcss/forms'),
  require('@tailwindcss/typography')
]
```

---

## 🧪 14. Customizing Tailwind

### 🧾 Extend Config

```js
theme: {
  extend: {
    colors: {
      primary: "#FF5722"
    },
    fontFamily: {
      roboto: ["Roboto", "sans-serif"]
    }
  }
}
```

---

## 💻 15. Reusable Components with `@apply`

```css
.btn {
  @apply px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600;
}
```

Use in HTML:

```html
<button class="btn">Click</button>
```

---

## 🎬 16. Animations & Transitions

```html
transition-all duration-500 ease-in-out
hover:scale-110
animate-pulse, animate-bounce, animate-spin
```

---

## 🧱 17. Shadows & Effects

```html
shadow-sm, shadow-md, shadow-lg
shadow-inner, shadow-2xl
drop-shadow-md, backdrop-blur-sm
```

---

## 📐 18. Aspect Ratio (via plugin)

```bash
npm install @tailwindcss/aspect-ratio
```

```html
<div class="aspect-w-16 aspect-h-9">
  <iframe ...></iframe>
</div>
```

---

## 📁 19. Container Utility

```html
<div class="container mx-auto px-4">
  Centered content with padding
</div>
```

---

## 🧼 20. Optimization & Production Build

### ✅ Remove unused styles

Tailwind uses **PurgeCSS** (enabled by default in newer versions):

```js
content: ["./src/**/*.{html,js}"]
```

---

## ✅ 21. Best Practices

* ✅ Use semantic HTML with Tailwind.
* ✅ Use utility-first, then extract into `@apply` when reused often.
* ✅ Use `prose` class with `@tailwindcss/typography` for blog-style content.
* ✅ Stick to mobile-first responsive design.
* ✅ Avoid unnecessary nesting. Keep class names clean.

---

## 🛠 22. Helpful Resources

* 🔗 [https://tailwindcss.com/docs](https://tailwindcss.com/docs)
* 🔗 [https://play.tailwindcss.com/](https://play.tailwindcss.com/)
* 🔗 [https://heroicons.com/](https://heroicons.com/)
* 🔗 [https://tailwindcomponents.com/](https://tailwindcomponents.com/)
* 🔗 [https://tailwindui.com/](https://tailwindui.com/) (Paid)

---

