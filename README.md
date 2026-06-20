# AMBS (Asset Management & Billing System)

A web-based, end-to-end encrypted (E2EE) inventory management system with integrated billing support and low inventory alerts. Designed for maximum efficiency and zero-knowledge privacy, AMBS ensures your business data remains entirely in your control.

🔗 **Live Demo:** [https://avm3005.github.io/AMBS](https://avm3005.github.io/AMBS)

---

## ✨ Features

* **End-to-End Encryption (E2EE):** Your data is locked behind a strict Encryption PIN. Only you can access it.
* **Flexible Storage Options:** 
  * **Local Account:** Saves directly to the device's storage for lightning-fast, offline-capable usage.
  * **Google Account:** Securely backs up your encrypted data to the cloud.
* **Smart Billing:** Dynamic pricing adjustments at the point of sale, with options to process sales with or without generating an official bill.
* **Inventory Control:** Automatic low and full stock alerts keep you on top of your supply chain.
* **Rapid Bill Sharing:** Share invoices instantly via WhatsApp, Email, SMS, or on-screen QR Code.
* **Speed Optimized:** Minimal image usage and full keyboard shortcut support for power users.

---

## 💻 Tech Stack

AMBS is built entirely with modern web technologies, prioritizing speed, light client-side execution, and cryptographic security.

* **Frontend Library:** React.js / Vue.js — Powering a dynamic, state-driven, and highly responsive user interface.
* **Styling & Icons:** 
    * Pure CSS / Tailwind CSS for a clean, modern UI with minimal image asset dependencies.
    * Lightweight SVG Icons (Heroicons/FontAwesome) for instant page loads.
* **Cryptographic Core:** Web Crypto API — Native browser API for secure, hardware-accelerated client-side encryption.
* **Database & Cloud Sync:** 
    * Firebase Authentication & Firestore (for Google Account cloud backups).
    * IndexedDB (for high-performance local caching and offline operations).
* **Utilities:**
    * Mousetrap.js / Custom Event Listeners for global keyboard shortcuts.
    * QRCode.js for dynamic client-side QR generation.

---

## 🛠️ Security Architecture

AMBS prioritizes absolute privacy. The system architecture is built around strict security failsafes:

1. **Zero-Knowledge Architecture:** During setup, you create a custom Encryption PIN used to encrypt all local and cloud data. **Warning: There is NO password or PIN reset option.** If you lose your PIN, your data is permanently unrecoverable.
2. **Brute-Force Failsafe:** For ultimate protection against unauthorized access, **5 consecutive incorrect PIN attempts will permanently delete your account and wipe all data.**
3. **Session Handling:** Encryption keys are flushed immediately from memory upon logout or tab closure.
4. **Data Portability:** Supports local import/export caching, allowing you to seamlessly migrate databases without relying on cloud connections.

---

## 🚀 Getting Started

### 1. Initial Setup
* Navigate to the [AMBS Web App](https://avm3005.github.io/AMBS).
* Choose your storage method: **Local Account** or **Google Account**.
* Enter your **Company Name** (defaults to dashboard view like "Nexus Inv").
* Set your **Encryption PIN**. *(Keep this safe!)*

### 2. Daily Operations
* **Login:** Enter your PIN. The E2EE protocol will activate and decrypt your dashboard.
* **Manage Inventory:** Add assets, set base prices, and define stock thresholds for automated alerts.
* **Process Sales:** 
  * Open the billing terminal using keyboard shortcuts.
  * Adjust prices dynamically and choose between "Sell With Bill" or "Sell Without Bill".
* **Share Invoices:** Click the share icon to send bills directly via WhatsApp or display a QR code for your customer.

---

## 🖥️ Application Modules (How the Sections Work)

AMBS is divided into several dedicated sections, each optimized for speed and specific business tasks:

### 1. Dashboard
The central hub for your business overview. 
* **Live Overview:** Displays quick metrics on daily sales and active stock.
* **Inventory Alerts:** Actively monitors your stock levels and pushes immediate notifications to the dashboard if an item reaches the "low stock" or "full stock" threshold defined in your inventory settings.

### 2. Inventory Management
Where you manage your physical assets and digital catalog.
* **Asset Entry:** Add new items, assign them categories, and set their base pricing.
* **Stock Control:** Manually adjust quantities or let the billing system deduct them automatically.
* **Dynamic Thresholds:** Set customized minimum and maximum stock limits for individual items to trigger alerts.

### 3. Billing Terminal (Point of Sale)
Designed for rapid transaction processing with minimal friction.
* **Keyboard Navigation:** Fully functional using keyboard shortcuts to speed up the checkout process without relying on a mouse.
* **Dynamic Pricing:** Modify the final selling price of any item directly in the cart (increase or decrease from the base price) before finalizing the sale.
* **Checkout Options:** 
  * *Sell With Bill:* Generates a formal invoice, logs the sale, and deducts inventory.
  * *Sell Without Bill:* Deducts the inventory and logs the revenue, but skips the invoice generation for faster, informal transactions.

### 4. Invoice & Sharing Hub
Handles the distribution of generated bills.
* **Digital Invoices:** Creates a clean, minimal-image digital receipt.
* **Multi-Channel Sharing:** Send the generated bill link directly to the customer via WhatsApp, SMS, or Email.
* **QR Code Generation:** Instantly displays a scannable QR code on your PC screen, allowing the customer to scan and download the bill directly to their mobile device.

### 5. Settings & Security
The control center for your data management and encryption protocols.
* **Storage Toggle:** Switch between Local Cache or Google Account syncing.
* **Data Migration:** Import or Export your encrypted database cache to easily move your setup between different computers.
* **Session Management:** Handles the E2EE background processes, ensuring your encryption key is flushed from memory the moment you exit the application.

---

## 🗺️ Development Roadmap

* **Stage 1 (Current):** Core PC UI, E2EE setup, basic storage (Local/Google), billing logic, and shortcut integration.
* **Stage 2:** Full mobile view optimization and streamlined WhatsApp bill-sharing integrations.
* **Stage 3:** Deep bug fixing, performance inspections, and stability enhancements across all viewports.
