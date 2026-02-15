## Core features:

- User authentication 
- Add job application
- Edit job application
- Delete job application
- View a list of all applications
- Application Informations (apply date, company, position, status)
- Data store in SQL Database
- CRUD operations via API Routes
- Responsive UI (desktop, mobile)

## Advanced features:

- Reminder system (maybe through an E-Mail?) for follow-up contact (e.g. for applications that have no answer for more than 2 weeks)
- Export & Import application to/from PDF
- Search Applcations
- Filter Applications

## User Stories

- As a user, I want to log in so that my data is saved securely.
- As a user, I want to log in so that I can access my applications.
- As a user, I want to add a job application so that I can track my progress.
- As a user, I want to edit an application so that I can update its status.
- As a user, I want to delete an application so that I can remove old entries.
- As a user, I want to see all my applications in one place so that I stay organized.
- As a user, I want to receive reminders so that I know when to follow up.
- As a user, I want to export my data so that I can share or store it.
- As a user, I want to import data so that I can use my backup file.
- As a user, I want to search ti applications and be able to filter through them.

## Basic workflow

1. User logs in.
2. User adds a new job application with details (company, position, date applied, etc.).
3. Application is saved in the database and displayed in the list.
4. User updates the application status as progress happens.
5. System checks for applications older than 2 weeks without updates and shows reminders.
6. User can export or import their applications list.
7. User logs out when finished.