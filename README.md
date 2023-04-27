# Ecoshop

A sustainable e-commerce application built with Vue.js 3, Tailwind CSS, and Firebase.

## Overview

This project is a comprehensive e-commerce app with a custom-built frontend and backend. It includes various features such as user authentication, product management, shopping cart functionality, order management, and data visualization.

### User Side

![User](https://firebasestorage.googleapis.com/v0/b/ecoshop-8b674.appspot.com/o/appScreenshots%2FScreenshot%202023-04-28%20at%201.26.41%20AM.png?alt=media&token=7603ceca-3a00-4c2a-a783-6f65a7c28682)
![User](https://firebasestorage.googleapis.com/v0/b/ecoshop-8b674.appspot.com/o/appScreenshots%2FScreenshot%202023-04-28%20at%201.27.02%20AM.png?alt=media&token=d0ece940-0db4-4f9c-a1c7-7f55f669e0a9)
![User](https://firebasestorage.googleapis.com/v0/b/ecoshop-8b674.appspot.com/o/appScreenshots%2FScreenshot%202023-04-28%20at%201.27.12%20AM.png?alt=media&token=f4bfc57f-3712-4cfb-bc52-e583846f8d53)

### Admin Side

![Admin](https://firebasestorage.googleapis.com/v0/b/ecoshop-8b674.appspot.com/o/appScreenshots%2FScreenshot%202023-04-28%20at%201.27.53%20AM.png?alt=media&token=a8ae4a04-6054-4629-af82-6b966ca65b09)

## Technologies

Project is created with:

- Vue.js 3 (Composition API)
- Tailwind CSS
- Firebase (Authentication, Firestore, Storage, and Functions)
- Algolia Search
- Chart.js

## Installation

1. Create a Firebase account: https://firebase.google.com/
2. Create an Algolia account: https://www.algolia.com/
3. Rename `.envSample` to `.env` and fill it with your Firebase and Algolia credentials.
4. Run `npm install`

## Diagrams

### Use Case Diagram

```mermaid
graph TD
   A((Customer)) --> B[Search Products]
   B --> C{Filter by Made Safe Certification}
   C --> D[View Product Details]
   D --> E[Add to Cart]
   E --> F[Checkout]
   F --> G[Select Payment Method]
   G --> H[Confirm Order]
   H --> I[Receive Order Confirmation]
   J((Vendor)) --> K[Add Product]
   K --> L[Request Made Safe Verification]
   L --> M[Update Product Status]
   N((Administrator)) --> O[Manage Users]
   O --> P[Approve Vendors]
   O --> Q[Manage Products]
   Q --> R[Verify Made Safe Certification]
   R --> S[Update Product Status]
   T((Made Safe Organization)) --> R
   X[EcoShop Sustainable E-Commerce Platform]
   X --> A
   X --> J
   X --> N
   X --> T
```

### Sequence Diagram
``` mermaid
sequenceDiagram
   participant Customer as Customer
   participant EcoShop as EcoShop
   participant Vendor as Vendor
   participant Administrator as Administrator
   participant MadeSafeOrganization as MadeSafeOrganization


   Customer ->> EcoShop: Browse Products
   EcoShop ->> Vendor: Request Products
   Vendor -->> EcoShop: Provide Products
   EcoShop -->> Customer: Display Products
   Customer ->> EcoShop: Add Product to Cart
   Customer ->> EcoShop: Checkout
   EcoShop ->> Vendor: Request Product Verification
   Vendor ->> MadeSafeOrganization: Request Verification
   MadeSafeOrganization -->> Vendor: Provide Verification
   Vendor -->> EcoShop: Update Product Status
   EcoShop ->> Administrator: Notify Product Status
   Administrator ->> EcoShop: Approve Product
   EcoShop -->> Customer: Send Order Confirmation
   EcoShop ->> Customer: Send Environmental Impact Report
```

## Info
All the products in the app are fake and for demonstration purposes only. If you proceed with an order, you will not be charged.
