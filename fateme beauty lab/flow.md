# Fatemeh Beauty Lab Website

## Functional Requirements & Workflow Document

Version: 1.0

---

# 1. Project Overview

The website is an e-commerce platform for Fatemeh Beauty Lab.

The platform has three primary business areas:

1. Product Sales
2. Facial Service Reservations
3. Educational and Consultation Services

The system should provide both customer-facing functionality and an administrative dashboard for content and business management.

---

# 2. User Roles

## 2.1 Customer

A registered or guest user who can:

* Browse products
* Search products
* Purchase products
* Submit consultation requests
* Reserve appointments
* Manage profile information
* View consultation responses

---

## 2.2 Administrator

Fatemeh and authorized staff members.

Administrator can:

* Manage products
* Manage categories
* Manage stories
* Manage appointments
* Manage consultation requests
* Manage banners
* Manage orders
* Manage users

---

# 3. Product Management

## Business Goal

Allow customers to purchase skincare products directly from the website.

---

## Functional Requirements

Administrator must be able to:

* Create products
* Edit products
* Delete products
* Archive products

Each product must contain:

* Title
* Description
* Images (multiple)
* Price
* Discount Price (optional)
* Inventory Count
* Product Category
* Product Gallery
* Status (Active / Inactive)

---

## User Flow

Customer enters website

→ Browse products

→ Open product page

→ Add product to cart

→ Proceed to checkout

→ Complete payment

→ Order created

→ Order displayed in admin panel

---

# 4. Product Categories

System must support separate category types.

## Category Types

### Product Categories

Examples:

* Serums
* Moisturizers
* Sunscreens

### Service Categories

Examples:

* Facial Treatments
* Skin Analysis
* Training Courses

Administrator can:

* Create categories
* Edit categories
* Delete categories

---

# 5. Story System

## Business Goal

Provide Instagram-like stories at the top of the website.

---

## Functional Requirements

Administrator can upload:

* Image Story
* Video Story

Video restrictions:

* Maximum duration: 30 seconds

Story properties:

* Title
* Media File
* Creation Date
* Expiration Date
* Status

---

## User Flow

User opens website

→ Story section displayed at top

→ User clicks story

→ Story opens in fullscreen viewer

→ Auto progresses to next story

---

## Backend Requirements

Stories should support:

* Multiple active stories
* Automatic expiration
* Story ordering
* Media optimization

---

# 6. Search System

## Business Goal

Allow users to quickly find products and services.

---

## Functional Requirements

Search must support:

* Product name
* Product category
* Service category
* Keywords

Filters:

* Category
* Price Range
* Availability

---

## User Flow

User enters search keyword

→ Search results displayed

→ User applies filters

→ Filtered results displayed

---

# 7. Shopping Cart

## Functional Requirements

Customer can:

* Add items
* Remove items
* Increase quantity
* Decrease quantity

Cart should display:

* Product Image
* Product Name
* Quantity
* Unit Price
* Total Price

---

## Checkout Flow

Cart

→ Checkout

→ Verify Profile Information

→ Verify Shipping Information

→ Payment

→ Order Creation

→ Order Confirmation

---

# 8. User Registration & Authentication

## Registration Flow

Step 1 (Required)

* First Name
* Last Name
* Mobile Number

System sends OTP.

User verifies OTP.

Account created.

---

## Step 2 (Optional)

User may enter:

* Province
* City
* Address
* Postal Code

---

## Checkout Validation

If shipping information is incomplete:

User must complete address information before payment.

---

# 9. Banner Management

Administrator can create homepage banners.

Banner properties:

* Title
* Subtitle
* Image
* Redirect URL
* Display Order
* Status

---

## Banner Types

### Product Category Banner

Redirects to product category pages.

### Service Category Banner

Redirects to service category pages.

---

# 10. Appointment Reservation System

## Business Goal

Allow customers to reserve facial treatment sessions.

---

## Admin Workflow

Administrator defines:

* Working Days
* Working Hours
* Reservation Duration
* Unavailable Dates

System generates available time slots.

---

## User Workflow

User selects service

→ Select date

→ Select available time

→ Enter information

→ Payment

→ Reservation Created

→ Reservation appears in Admin Panel

---

## Reservation Data

* Reservation ID
* User
* Service
* Date
* Time
* Payment Status
* Reservation Status

---

## Reservation Statuses

* Pending
* Confirmed
* Completed
* Cancelled

---

# 11. Consultation Request System

## Business Goal

Provide paid online skincare consultation.

---

## User Workflow

User enters consultation page

→ Completes consultation form

→ Consultation created

→ Awaiting response

---

## Consultation Form Fields

Examples:

* Full Name
* Age
* Skin Type
* Skin Problems
* Current Routine
* Additional Notes
* Photo Uploads (Optional)

---

## Consultation Statuses

* Pending complete form
* Waiting For Review
* Answered
* Closed

---

## Admin Workflow

Administrator opens consultation request

→ Reviews submitted information

→ Writes consultation response

Response editor should support:

* Rich Text
* Product Links
* Appointment Booking Links

---

## Customer Notification

After response submission:

System sends SMS notification.

Message example:

"Your consultation response is ready."

Customer logs in

→ Opens consultation page

→ Views response

---

# 12. Orders Management

Administrator can:

* View Orders
* Change Order Status
* View Customer Information
* Print Orders

---

## Order Statuses

* Pending Payment
* Paid
* Processing
* Shipped
* Delivered
* Cancelled

---

# 13. Admin Dashboard

Administrator dashboard should include:

## Statistics

* Total Orders
* Total Revenue
* Total Users
* Total Reservations
* Total Consultation Requests

---

## Management Modules

* Products
* Categories
* Stories
* Banners
* Orders
* Users
* Reservations
* Consultation Requests

---

# 14. SMS Notifications

System should support SMS notifications for:

* OTP Verification
* Successful Order
* Reservation Confirmation
* Consultation Response Ready

---

# 15. Payment Gateway

All paid services must use a unified payment gateway.

Supported payments:

* Product Purchases
* Consultation Requests
* Appointment Reservations

---

# 16. Future Scalability

The architecture should allow future implementation of:

* Loyalty Club
* Discount Codes
* Gift Cards
* Course Sales
* Blog System
* Push Notifications
* Customer Reviews
* Wishlist
* Product Recommendations

---

# 17. Non-Functional Requirements

## Performance

* Mobile First
* Responsive Design
* Optimized Images
* Lazy Loading

## Security

* JWT Authentication
* OTP Verification
* Rate Limiting
* Input Validation

## SEO

* SEO Friendly URLs
* Meta Tags
* Sitemap
* Structured Data

## Media Storage

Store uploaded images/videos using cloud object storage.

Examples:

* AWS S3
* Cloudflare R2
* MinIO

---

# End of Document
