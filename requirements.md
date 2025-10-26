# Airbnb Clone – Backend Requirement Specifications

## 1. User Authentication
### Functional Requirements
- Users must register with name, email, and password.
- Passwords must be encrypted using bcrypt.
- JWT tokens used for session management.

### API Endpoints
| Method | Endpoint          | Description |
|--------|-------------------|-------------|
| POST   | /api/register     | Create new user |
| POST   | /api/login        | Authenticate user |

---

## 2. Property Management
### Functional Requirements
- Hosts can create, edit, or delete properties.
- Each property must include title, location, price, and availability.

### API Endpoints
| Method | Endpoint          | Description |
|--------|-------------------|-------------|
| POST   | /api/properties   | Add new property |
| GET    | /api/properties   | Fetch all properties |
| PUT    | /api/properties/:id | Update property |
| DELETE | /api/properties/:id | Remove property |

---

## 3. Booking System
### Functional Requirements
- Guests can book available properties.
- Prevent double bookings on overlapping dates.

### API Endpoints
| Method | Endpoint         | Description |
|--------|------------------|-------------|
| POST   | /api/bookings    | Create booking |
| GET    | /api/bookings    | View all bookings |

---

## Non-Functional Requirements
- Response time < 500ms for all requests.
- Database: PostgreSQL/MySQL.
- Authentication: JWT.
- Security: HTTPS & password hashing.
