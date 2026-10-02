# Lab 3 - Architectural Style Analysis

## System
Vaccination Cohort & Dose Scheduling System (continued from Lab 1).

## Architecture styles considered
- **Layered Architecture:** Presentation, Business, and Data layers with clear separation of concerns. The handout notes easier understanding/maintainability, with possible performance overhead.
- **Microservices Architecture:** independently deployable services with independent scaling and fault isolation, but with greater operational complexity, network latency, and data-consistency challenges.
- **Client-Server Architecture:** centralized server with multiple clients, offering centralized control and simple deployment, but introducing a single point of failure and a possible scalability bottleneck.

## Selected style
**Layered Architecture**

The selection follows the structure of the Lab 1 system: citizen registration/profile management, dose scheduling and interval validation, vaccination recording, QR certificate generation/verification, and protected vaccination data.

## Components
1. Citizen Portal
2. Appointment Management
3. Vaccination Record
4. Certificate & QR Verification
5. Authentication & Access Control
6. Vaccination Database
7. Vaccination Officer UI

## Interfaces / interactions
- Appointment API
- Citizen Record API
- Certificate Request API
- Data Access
- Auth Token
- Dose Booking / Status
- Vaccination Entry
- Officer Record API

## Security and performance
Authentication and access control provide a clear boundary before sensitive operations reach citizen vaccination data. The certificate/QR verification path is kept focused so it can be measured against the Lab 1 verification performance target.
