🐾 D.A.R.T — Dodo Animal Rescue Team

A full-stack web application for managing street animal rescues, donations, and care tracking — built for Kothrud, Pune.
---

About the Project: 
D.A.R.T (Dodo Animal Rescue Team) is a community platform that allows:
- The public to report injured street animals needing rescue
- Donors to contribute funds toward specific animals' medical care
- Admins to view and manage all animals, rescues, and donations
---

### Backend
| Technology | Purpose |
|---|---|
| Java 17 | Programming language |
| Spring Boot 4.0.5 | Backend framework |
| Spring Web MVC | REST API |
| Spring Data JPA | Database ORM |
| Spring Security | API access control |
| MySQL | Database |
| Lombok | Reduces boilerplate code |
| Maven | Build tool |

### Frontend
| Technology | Purpose |
|---|---|
| React 19 | UI library |
| Vite 8 | Build tool & dev server |
| React Router DOM 7 | Client-side routing |
| Axios | HTTP requests to backend |
| Tailwind CSS 3 | Styling |

The backend starts on "http://localhost:8080". The database `dart_db` is created automatically, and sample data is loaded from `data.sql`.

The frontend starts on "http://localhost:5173".
---

API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/animals` | Get all animals |
| POST | `/api/animals` | Add a new animal |
| GET | `/api/rescues` | Get all rescue reports |
| POST | `/api/rescues` | Submit a rescue report |
| GET | `/api/donations` | Get all donations |
| POST | `/api/donations` | Submit a donation |
| POST | `/api/auth/login` | Admin login |

---
#Database Schema

animals — stores rescued animal profiles with name, species, status, and donation goal/progress
rescues — stores public rescue reports with location, description, and reporter contact
donations — stores donor contributions linked to a specific animal; automatically updates the animal's `donationRaised` field
