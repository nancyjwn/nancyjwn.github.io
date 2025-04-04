---
title: "Create an E-Ticket Event System with Laravel"
date: 2024-12-05
categories: [Web Development]
tags: [Laravel, PHP, Tailwind CSS, Flowbite]
author: Nancy Jiwono
layout: post
description: "Learn how to create an E-Ticket booking system using Laravel, a powerful PHP framework."
image: /assets/eticket/coverTicket.png
comments: true
---

## 📖 Project Description  
This project is a **web-based e-ticketing system** designed to simplify **event management, ticket booking, and user interactions** for different types of users, including **admins, event organizers, registered users, and general visitors**. The system allows users to **search for events, book tickets, view booking history, and save favorite events**. Additionally, admins and event organizers can **manage events, tickets, and sales reports**.  

The system also supports additional features such as **real-time ticket availability tracking, event review system, and analytics** to provide insights to admins and organizers about event performance.  

## Key Features 
#### **1. User Management (UI)**  
**Admin:**  
- Manage users (**CRUD** - Create, Read, Update, Delete).  
- Create new users with roles (**admin, event organizer, or regular user**).  
- Remove inactive users.  

**Event Organizer:**  
- No access to user management.  

**Registered User:**  
- Manage their own profile.

#### **2. Event Management**  
**Admin & Event Organizer:**  
- Create, edit, and delete events.  
- Add event details such as **name, description, date, time, location, ticket price, ticket quota, and event images**.  
- View a list of created events.  

#### **3. Ticket Booking**  
**Registered User:**  
- Book tickets for specific events.  
- View their ticket booking history.  
- Cancel ticket bookings if within the allowed cancellation period.  

#### **4. Favorite Events**  
**Registered User:**  
- Save events to their **favorites list**.  
- View their **saved favorite events**.  

#### **5. Reports & Analytics**  
**Admin & Event Organizer:**  
- View **ticket sales reports** for specific events.  
- Display **data** such as **total tickets sold, total revenue, and booking status**.  
- Provide **charts and statistics** related to event performance (optional).  

#### **6. Event Rating & Review**  
**Registered User:**  
- Leave **reviews and ratings** for attended events.  

#### **7. Real-Time Availability Tracker**  
**All Users:**  
- Display the **real-time number of available tickets** for each event.

## User Structure & Usage Flow
#### **1. Admin**  
- Has full access to all system features.  
- Manages **users, events, tickets, and reports**.  
- Views **statistics and analytics** related to event performance.  
- Logs in as an **admin** to oversee the system.  

### **Admin Dashboard Features**  
The admin dashboard provides powerful tools for managing the system, including:  
- 📝 **Event Management**: Create, update, and delete events.  
- 📊 **Reports & Analytics**: View ticket sales reports and user activity analytics.  

![Admin Dashboard Overview](/assets/eticket/adminDashboard.png)  
*Figure 1: The admin dashboard provides an overview of system management, including quick access to user, event, and report management tools.*  

![User Management Dashboard](/assets/eticket/adminUser.png)  
*Figure 2: The user management section allows admins to create, update, and delete user accounts, as well as assign roles such as admin, organizer, or user.*  

![Event Management Dashboard](/assets/eticket/adminEvent.png)  
*Figure 3: The event management section enables admins to create, edit, and delete events, as well as manage event details like date, location, and ticket quotas.*  

![Reports and Analytics Dashboard](/assets/eticket/adminGrafik.png)  
*Figure 4: The reports and analytics section provides insights into ticket sales, revenue, and user activity through charts and statistics.*  

#### **2. Event Organizer**  
- Creates and manages their **own events**.  
- Views **ticket booking lists** for their events.  
- Cannot **edit or delete** events created by other organizers.  
- Logs in as an **organizer**, creates events, and monitors ticket sales.  

#### **3. Registered User (Pengguna Terdaftar)**  
- Creates an **account**, logs in, and **books tickets**.  
- Views **booking history and status**.  
- Saves events to their **favorites list**.  
- Can cancel **ticket bookings** if within the allowed cancellation window.  

#### **4. Guest (Pengunjung Umum)**  
- Views the **event list and details** on the homepage.  
- Clicks **"View Details"** to check event information.  
- Must **log in or register** to book tickets or save events to favorites.

## Layout and User Interface
#### **1. Login/Register Page**  
- Login page for **admin, event organizers, and registered users**.  
- Registration page for **new users**.  

#### **2. Homepage**  
- Displays **latest and popular events**.  
- Search bar to find events by **name, category, or location**.  

#### **3. Event Catalog**  
- Showcases all events with **previews (name, image, date, and location)**.  
- Includes **filter and sorting** options by **category, location, or date**.  

#### **4. Event Details Page**  
- Provides **detailed event information**: name, description, time, location, ticket price, and ticket quota.  
- **"Book Ticket"** button for registered users or redirect to **login page** for guests.  
- Option to **save the event to favorites**.  

#### **5. User Dashboard**  
- **Profile Management**: Manage account information.  
- **Booking History**: View list of ticket bookings and their status.  
- **Favorite Events**: Displays saved events.  

#### **6. Admin Dashboard**  
- **Manage Users**: Handle user accounts and roles.  
- **Manage Events**: Create, update, and delete events.  
- **Reports**: View ticket sales reports and user activity analytics.  

#### **7. Organizer Dashboard**  
- **Manage Events**: CRUD functionality for events created by the organizer.  
- **View Bookings**: See ticket bookings for their events.  

## 🛠️ Technology Stack
#### 1. **Backend**  
- **Framework**: Laravel (PHP).  
- **Database**: MySQL or other Laravel-supported databases.  
- **ORM**: Eloquent ORM for database management.  

#### 2. **Frontend**  
- **Template Engine**: Blade (Laravel).  
- **CSS Framework**: Tailwind CSS or another responsive design framework.  
- **JavaScript**: For additional interactivity.  

#### 3. **Tools and Libraries**  
- **Flowbite**: For additional UI components.  
- **Middleware**: To manage access based on user roles.

## 📂 File Structure 
#### **1. User Management**  
- **Controller**: `AdminController.php`  
- **Model**: `User.php`  
- **View**: `resources/views/admin/users/*`  
- **Route**: `web.php`  

#### **2. Event Management**  
- **Controller**: `AdminController.php`, `OrganizerDashboardController.php`  
- **Model**: `Event.php`  
- **View**:  
  - `resources/views/admin/events/*`  
  - `resources/views/organizer/events/*`  
- **Route**: `web.php`  

#### **3. Ticket Booking**  
- **Controller**: `UserDashboardController.php`  
- **Model**: `Booking.php`  
- **View**: `resources/views/dashboard/user/bookings/*`  
- **Route**: `web.php`  

#### **4. Favorites**  
- **Controller**: `UserDashboardController.php`  
- **Model**: `Favorite.php`  
- **View**: `favorite.blade.php`  
- **Route**: `web.php`  

#### **5. Reports & Analytics**  
- **Controller**: `AdminController.php`, `OrganizerDashboardController.php`  
- **Model**: `Booking.php`  
- **View**:  
  - `resources/views/admin/reports/*`  
  - `resources/views/organizer/reports/*`  
- **Route**: `web.php`  

