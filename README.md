# AI-Powered-Roadmap-Timetable-Generator

AI-Powered Roadmap & Timetable Generator
This application is a real-time, AI-powered tool designed to help users create personalized learning roadmaps and study timetables based on their learning goals, availability, and skill level. It leverages the power of generative AI to dynamically generate study plans and integrates with Firestore for real-time data persistence and progress tracking.

🔍 Concept Overview
Users input a learning goal or topic (e.g., "I want to learn Java backend development"), and the app:

Uses AI (Gemini API) to generate a personalized roadmap with key topics/modules, including estimated hours, difficulty, and relevant resources.

Automatically creates a study timetable/calendar based on:

User's daily availability (hours per day)

A specified deadline/goal time

An option to exclude weekends from the schedule.

🌟 Key Features
Real-time & Personalized Roadmaps: Generates dynamic study plans tailored to individual user inputs.

AI Integration: Utilizes the Gemini API to dynamically create study modules, descriptions, estimated times, difficulty levels, and relevant learning resources (links).

Time-based Structuring: Organizes learning modules into a daily timetable to aid motivation, productivity, and progress tracking.

Applicability: Versatile for any topic – coding, design, languages, academic subjects, etc.

Progress Tracking: Users can mark modules as "completed," and an overall progress bar visually tracks their learning journey.

Drag-and-Drop Rescheduling: Allows users to reorder modules within a specific day's timetable for flexibility.

Weekend Exclusion: Option to generate timetables that only include weekdays.

Notifications (Basic): Provides a button to enable browser notifications for study reminders.

Data Persistence: Uses Google Firestore to save user-generated roadmaps and timetables, allowing data to persist across sessions and devices (for the same user ID).

🧠 Core Functionality
Input Interface:

Topic: User's learning goal (e.g., "React Native development").

Deadline: Target completion date.

Hours/day: Daily study commitment.

Skill Level: Beginner / Intermediate / Advanced.

Exclude Weekends: Checkbox to omit weekend study days.

AI Engine: Makes a fetch call to the Gemini API with a structured prompt to generate a JSON array of learning modules, each with title, description, estimatedHours, difficulty, prerequisites, and resources (title and URL).

Timetable Generator: Schedules the AI-generated modules over the user's timeline, respecting daily hours and weekend preferences.

Progress Tracker: Calculates and displays the percentage of completed modules.

Drag-and-Drop: Implemented for reordering items within a day's schedule.

Notifications: Basic browser notification permission request and a test notification.

🛠️ Tech Stack
Frontend: HTML, CSS (Tailwind CSS), JavaScript (Vanilla JS)

AI Integration: Google Gemini API (gemini-2.0-flash)

Data Persistence: Google Firestore (for real-time sync and storage)

Authentication: Firebase Authentication (anonymous sign-in, with custom token support for Canvas environment)

🚀 How to Use
Enter Your Learning Goal: Type the topic or skill you wish to learn into the "Learning Topic/Goal" field.

Set Your Deadline: Choose a date by which you aim to complete your learning.

Specify Hours per Day: Input the number of hours you can dedicate to studying daily.

Select Your Skill Level: Choose your current proficiency in the topic.

Exclude Weekends (Optional): Check this box if you prefer your timetable to only include weekdays.

Generate Plan: Click the "Generate Roadmap & Timetable" button.

Track Progress: Use the checkboxes next to each module in the roadmap and timetable to mark them as completed. The overall progress bar will update.

Reorder Timetable: Drag and drop module items within a day's list in the "Your Study Timetable" section to change their order.

Enable Notifications: Click the "Enable Notifications" button to allow browser notifications for reminders.

💡 Future Enhancements
Multi-day Drag-and-Drop: Implement more sophisticated drag-and-drop to move modules between different days, with intelligent hour redistribution.

User Accounts: Full user authentication (email/password, social logins) for personalized dashboards and multi-device access.

Advanced Notification Scheduling: Integrate a more robust system for scheduling and managing daily study reminders.

Gamification: Add XP points or badges for completing modules/days.

Export & Share: Functionality to export the roadmap as PDF/image or generate shareable links.

Editable Modules: Allow users to manually edit module details (title, description, hours).

Feedback Loop: Enable users to provide feedback on AI-generated content to improve future suggestions.
