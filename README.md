# 🎓 The Helper: Smart College Management System

**The Helper** is a full-stack native Android application designed to bridge the communication gap between College Administration, Faculty, and Students. It utilizes **Firebase** for real-time data synchronization and Role-Based Access Control (RBAC) to ensure secure and targeted resource distribution.

## 📱 Project Overview

In a traditional college setting, distributing digital notes (PDFs) to specific batches is chaotic. Teachers often struggle to ensure that "Computer Science Semester 3" notes don't get mixed up with "Mechanical Semester 5".

**The Helper** solves this using a **Dynamic Key Generation** algorithm. The app automatically maps a student's profile to the correct database node, creating a zero-friction experience where students only see content relevant to their academic journey.

## 🚀 Key Features

### 🔐 1. Role-Based Access Control (RBAC)
The app features three distinct dashboards based on user privileges:

* **Admin:**
    * Exclusive authority to register Teachers and Students (ensuring database integrity).
    * Ability to post global Notices visible to the entire college.
* **Teacher:**
    * Dynamic dashboard to upload **PDF Notes, Assignments, and Question Banks**.
    * Categorized uploads based on Branch (e.g., CSE, Civil) and Semester.
* **Student:**
    * **Auto-Personalized Feed:** No need to search or filter. The app detects the student's profile and auto-fetches the correct materials.
    * View and Download study resources securely.

### 🧠 2. Smart "Many-to-Many" Data Mapping
This is the core engineering highlight of the project.
* **Write Path:** When a teacher uploads a file, the app generates a composite key (e.g., `CSE_3`) and stores the file metadata at `Materials/CSE_3/Category`.
* **Read Path:** When a student logs in, the app extracts their PRN from their email, queries their profile to find their Branch (`CSE`) and Semester (`3`), cleans the strings, and automatically attaches a listener to `Materials/CSE_3`.

## 🛠️ Tech Stack

* **Language:** Java (Native Android)
* **Architecture:** MVC (Model-View-Controller)
* **Database:** Firebase Realtime Database (NoSQL JSON)
* **Storage:** Firebase Cloud Storage (PDF Document handling)
* **Authentication:** Firebase Auth (Email/Password)
* **UI Components:** CardViews, RecyclerViews, Spinners, Fragments

## 📸 Screenshots

Teacher Dashboard |Student View |
 Admin Panel |

![WhatsApp Image 2026-01-08 at 10 42 20 PM](https://github.com/user-attachments/assets/9c331c7f-9301-4ff1-bde9-f7c9095a4f6a)
 
 
![WhatsApp Image 2026-01-12 at 10 42 28 PM](https://github.com/user-attachments/assets/c5168c58-306b-4c6b-86cd-c3425d427346)
 
 | ![WhatsApp Image 2026-01-12 at 10 42 29 PM](https://github.com/user-attachments/assets/63a65b64-d710-4fc5-a96d-ae1f6e7492c5)
|

## ⚙️ Installation & Setup

1.  Clone the repository:
    ```bash
    git clone [https://github.com/nishantkushwaha76/The-Helper-College-App.git](https://github.com/nishantkushwaha76/The-Helper-College-App.git)
    ```
2.  Open the project in **Android Studio**.
3.  **Important:** You must create your own Firebase Project.
    * Download `google-services.json` from your Firebase Console.
    * Place it in the `app/` directory.
4.  Sync Gradle and Run.

---
*Built with  by Nishant Kushwaha*
