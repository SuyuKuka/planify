# Planify

## About

**Planify** is a web platform designed to streamline meeting planning and scheduling developed as a third-year Bachelor's (L3 Informatique) project at Université Paris Cité. Built from scratch, this project allows users to propose meeting slots, invite participants, import `.ics` calendars to cast their votes immediately, and find the best common dates.

The project features user authentication, email-based voting links for participants without an account, profile management, and calendar integration.

*Note: As this was an academic project, the codebase and user interface are primarily in French.*

## Tech Stack
- **Backend:** Node.js, Express
- **Template Engine:** EJS
- **Frontend/UI:** Bootstrap, jQuery, CSS3
- **Database:** PostgreSQL
- **Build System / Tooling:** npm

## Key Features
- **Meeting Creation & Management:** Organizers can propose multiple date slots and invite participants.
- **Flexible Participant Voting:** Registered users or invited guests (via a unique secure email link without a required account) can vote on time slots.
- **Calendar `.ics` Import:** Seamlessly import `.ics` calendar files to automatically analyze availabilities and vote immediately.
- **User Authentication:** Secure sign-up, login, and password recovery via email notifications.
- **Account Management:** Ability to update user profile information, passwords, and profile pictures.
- **User Directory & Search:** Search bar feature to easily look up other users and accounts on the platform.

## Project Structure

```text
📁 planify
│
├── 📁 config                        # Configuration files
│   └── 📁 database/                 # Database connection and setup files
|
├── 📁 entities/                     # Data models and business logic entities
│   ├── 📁 auth/                     # Authentication and session entities
│   ├── 📁 index/                    # Home/Landing page related entities
│   └── 📁 user/                     # User profile and account entities
│
├── 📁 public/                       # Static assets accessible to the browser
│   ├── 📁 css/
│   │   ├── 📁 auth/                 # Styles specific to authentication pages
│   │   ├── 📁 index/                # Styles for the home/landing page
│   │   └── 📁 user/                 # Styles for user interface sections
│   ├── 📁 images/                   # Assets 
│   │   └── 📁 profile/              # User profile pictures and avatars
│   └── 📁 js/                       # Client-side JavaScript scripts
│       ├── 📁 auth/                 # Auth-related frontend logic
│       ├── 📁 client_server_shared/ # Code shared between client and server
│       ├── 📁 index/                # Home/Landing page scripts
│       └── 📁 user/                 # User-related frontend scripts
|
├── 📁 services/                     # External API integrations
|
├── 📁 views/                        # Frontend templates (HTML/UI views)
│   ├── 📁 auth/                     # Login, register, and auth views
│   ├── 📁 index/                    # Home/Landing page views
│   └── 📁 user/                     # User dashboard and profile views
│
├── 📄 .env                                       # Environment variables configuration
├── 📄 app.js                                     # Main application entry point & server setup
├── 📄 LICENSE                                    # License of the project
├── 📄 package-lock.json / package.json           # Dependencies & scripts
├── 📄 planify.sql                                # SQL database
└── 📄 README.md                                  # Project documentation
```

## Getting Started

### Prerequisites
- **Node.js** (v16 or higher recommended)
- **PostgreSQL**
- **npm** (Node Package Manager)
- A modern web browser

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/your-username/planify.git
cd planify
```

2. **Install dependencies (Frontend & Backend):**
```bash
npm ci .
```

3. **Configure environment variables:**  
Create a `.env` file in the root directory and add your configuration:
```env
DB_USER=yourusername
DB_HOST=localhost
DB_NAME=planify
DB_PASSWORD='yourpassword'
DB_PORT=5432
```

4. **Connect to PostgreSQL:**  
Access your PostgreSQL interactive terminal using your database credentials:
```bash
psql -U yourusername -d planify
```

5. **Initialize the database:**  
Import the provided SQL schema file into your database:
```sql
\i planify.sql
```

6. **Launch the application:**
```bash
node app.js
```

7. **Cleaning**
```bash
rm -rf node_modules
```

## Usage

Once the application is running, open your browser and navigate to: `http://localhost:8080`

## Team

This project was developed collaboratively as a 2-person team:

- **CHEN Michel** - Full-Stack Development & Architecture 
  [![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github)](https://github.com/SuyuKuka)
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-0A66C2?logo=linkedin)](https://linkedin.com/in/chen-michel)


- **CHIV Henri** - Full-Stack Development & Architecture 
  [![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github)](https://github.com/H-flamme)

## License

This project was developed for academic purposes at **Université Paris Cité** and is provided for portfolio demonstration purposes. 

**Code:** The source code of this project is open-source and available under the GPL 3.0 License — see [LICENSE](LICENSE) for details.

**Assets:** Images assets (such as icons, etc) belong to their respective copyright owners. They are included here strictly for educational and portfolio demonstration purposes and are not distributed under an open-source license.