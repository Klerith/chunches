# Chunches — Family Life, Organized Together

> The app that keeps your family in sync — from the grocery run to the weekend trip.

Chunches brings every corner of family planning into one shared space. Real-time collaboration, smart tools, and a design everyone will actually enjoy using.

---

## Table of Contents

1. [Shopping Lists](#shopping-lists)
2. [Family Recipes](#family-recipes)
3. [Family Calendar](#family-calendar)
4. [Places & Recommendations](#places--recommendations)
5. [Family Hub](#family-hub)
6. [Push Notifications](#push-notifications)
7. [Calendar Sync](#calendar-sync)
8. [Personalization](#personalization)
9. [Authentication](#authentication)
10. [Availability](#availability)

---

## Shopping Lists

> Never forget an ingredient. Never buy duplicates. Always in sync.

<!-- PHOTO: Main lists screen showing multiple colored list cards -->

### Create & Organize

- Create as many shopping lists as you need — one for groceries, one for the hardware store, one for the holiday trip.
- Each list has a **custom color** so you can tell them apart at a glance.
- Pin your most-used list to the top for quick access.

### Smart Item Entry

- Type items naturally — Chunches **automatically parses quantity and units** (e.g., "2 kg apples" becomes qty: 2, unit: kg, name: apples).
- Items are **automatically grouped by category**: Vegetables, Dairy, Meat, Beverages, Snacks, and more — no manual sorting needed.
- Add a **product link** to any item for easy price comparison before you shop.

<!-- PHOTO: List detail screen with items grouped by category -->

### Real-Time Collaboration

- Every family member sees **live updates** the moment someone adds or checks off an item.
- Check off items as you shop — the rest of the family sees it happen in real time.
- **Clear completed items** with one tap once you're done at the store.

---

## Family Recipes

> Your family's cookbook, always at hand — and connected to your shopping list.

<!-- PHOTO: Recipes grid with meal photos -->

### Discover & Browse

- Browse the full family recipe collection with **photo cards**.
- Filter by **meal type** (Breakfast, Lunch, Dinner, Snack, Dessert) or **difficulty** (Easy, Medium, Hard).
- **Full-text search** finds any recipe in seconds.

### Recipe Details

- Each recipe includes: title, description, prep and cook time, servings, difficulty, and meal type.
- **Ingredients** are listed with quantities and units, organized by category.
- **Step-by-step cooking instructions** — numbered and easy to follow.

<!-- PHOTO: Recipe detail screen showing ingredients and steps -->

### Seamless Shopping Integration

- Tap **"Add to List"** on any recipe to send all its ingredients directly to a shopping list.
- Choose which list to add to — Chunches does the rest.

### Ratings & Community

- Rate any recipe 1–5 stars.
- See the **average family rating** on every recipe card.

### Create Your Own

- Add new recipes with a photo, description, ingredients, and step-by-step instructions.
- Upload a cover photo from your camera or gallery.
- Edit and update recipes any time.

---

## Family Calendar

> One calendar for the whole family. No more "I didn't know about that."

<!-- PHOTO: Calendar screen in month view with event dots -->

### Interactive Calendar View

- Beautifully designed calendar that switches between **month, 2-week, and week views**.
- Drag the handle to expand or collapse the calendar — more room for event details below.
- Color-coded event dots make busy days easy to spot.
- Tap **Today** to jump back to the current date instantly.

### Events at a Glance

- Events appear as cards below the calendar, grouped by day.
- Each event shows its **title, time, creator, color, and icon** for instant recognition.

<!-- PHOTO: Event cards below the calendar -->

### Rich Event Details

- Add a title, date, time, description, URL, and address to any event.
- Choose from **16+ icons** and **8 colors** so every event has its own personality.
- Optional **recurrence rules**: daily, weekdays, weekends, or weekly.
- Set a recurrence end date when needed.

### Event Reminders

- Get a **push notification** before any event — 15 minutes, 30 minutes, 1 hour, or more.
- Reminders are fully **timezone-aware**, so they fire at the right local time no matter where you are.

---

## Places & Recommendations

> Save the places your family loves — restaurants, parks, hidden gems.

<!-- PHOTO: Places grid showing cards with photos and categories -->

### Your Family's Curated Map

- Build a shared directory of **favorite places** — restaurants, cafés, parks, museums, playgrounds, pools, and more.
- Each place has a cover photo, name, category, and visit status.
- See at a glance which places your family has already visited.

### Rich Place Profiles

- Store the **address** (parsed directly from a Google Maps link), phone number, website, and opening hours.
- Tap the address to **open directions** in Google Maps.
- Add a **description** and choose from a set of tags: Family-friendly, Kids, Pets, Accessible, Parking, Outdoor, Budget-friendly, Photo-worthy, and more.

<!-- PHOTO: Place detail screen with photo gallery and notes -->

### Photos & Notes

- Upload multiple photos to build a **visual gallery** for each place.
- Add **notes** to record memories, tips, or anything the family should know — with timestamps and author names.

### Visit Tracking

- Mark a place as **visited** with one tap. The visit date is recorded automatically.
- Filter the list to show only visited (or yet-to-visit) places.

---

## Family Hub

> Invite anyone. Manage your family in seconds.

<!-- PHOTO: Family screen with member list and invite options -->

### Create or Join a Family

- Start a new family space or join an existing one via invite.
- All content — lists, recipes, events, places — is **shared with every family member** automatically.

### Effortless Invites

- Generate a **6-character invite code** or a **QR code** — share either one to bring someone in.
- Share the code via **WhatsApp, iMessage, email**, or any app on your phone.
- Invites expire after 30 days and support usage limits.
- **Regenerate the code** at any time to revoke old invites.

<!-- PHOTO: Invite QR code screen -->

### Joining Flow

- Tap an invite link and see a **preview of the family** (name, color, member count) before accepting.
- Accepting automatically syncs all shared content to the new member's app.
- Works with deep links (`chunches://join/CODE`) and web links.

### Member Management

- See all family members with their avatars and names.
- Remove members when needed, with a confirmation step.

---

## Push Notifications

> Stay in the loop — without constantly checking the app.

<!-- PHOTO: Notification preferences screen -->

### Activity Alerts

- Get notified when a family member **adds items to a list**, **posts a new recipe**, **creates an event**, **saves a new place**, or **joins the family**.
- Each notification type can be **independently toggled on or off**.

### Event Reminders

- Receive a push reminder before any calendar event.
- Choose your preferred lead time: **15 minutes, 30 minutes, 1 hour, 2 hours**, or more.
- Works even when the app is closed.

### Smart Delivery

- Powered by **Firebase Cloud Messaging** for reliable delivery on iOS and Android.
- Tapping a notification **deep-links directly** to the relevant screen — list, recipe, event, or place.

---

## Calendar Sync

> Chunches events, right inside your device calendar.

<!-- PHOTO: Calendar sync settings screen -->

- Enable **one-way sync** to push all family events into Apple Calendar, Google Calendar, or any other calendar on your device.
- Choose which device calendar to sync to.
- Events **update automatically** when they change in Chunches — no manual refresh needed.
- Sync is fully **timezone-aware**.

---

## Personalization

> Your app, your look.

<!-- PHOTO: Color theme picker screen -->

### Themes & Colors

- Choose between **Light, Dark, or System** (follows your device setting).
- Pick from **9 accent colors**: Purple, Green, Blue, Pink, Orange, Teal, Red, Indigo, and Amber.
- The entire app adapts — buttons, icons, cards, and backgrounds — with a consistent Material Design 3 palette.

### Language

- Available in **English, Spanish, French, and Italian**.
- Or follow your device's system language automatically.

### Profile

- Set a **display name** and upload a **profile photo** (from gallery or camera).
- Change your password or sign out at any time.

---

## Authentication

> Simple, secure sign-in — your way.

<!-- PHOTO: Onboarding screen -->

- **Google Sign-In** — one tap, no passwords.
- **Apple Sign-In** — native iOS integration.
- **Email & Password** — classic sign-up with email confirmation.
- **Forgot password?** — recover your account via email link in seconds.

---

## Availability

| Platform            | Status                     |
| ------------------- | -------------------------- |
| iOS (iPhone & iPad) | Available on the App Store |
| Android             | Coming soon                |

---

## Built for Real Families

Chunches is designed around one idea: **everything your family plans, decides, and saves should be in one shared place**. No more scattered notes, forgotten grocery items, or missed events. Just one app, always in sync.

<!-- PHOTO: Family using the app together -->

---

_Made with care for families everywhere._
