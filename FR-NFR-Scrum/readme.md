### **Introduction**

Requirements define what a system must do (functional) and how well it should perform those tasks (non-functional). Properly capturing both types is essential for delivering a successful software product that meets user needs and quality expectations.

---

## **Step-by-Step Guide to Working with Functional & Non-Functional Requirements**

### **Step 1: Understand the Problem Domain**
- Engage stakeholders (users, clients, business analysts, developers).
- Conduct interviews, workshops, or surveys.
- Document high-level goals and pain points.

### **Step 2: Identify Functional Requirements (FRs)**
- Ask: *“What should the system do?”*
- Focus on features, behaviors, inputs, outputs, and interactions.
- Use techniques like user stories, use cases, or process flows.
- Ensure each FR is:
  - **Specific**
  - **Testable**
  - **Traceable**
  - **Unambiguous**

### **Step 3: Identify Non-Functional Requirements (NFRs)**
- Ask: *“How well should the system perform its functions?”*
- Consider quality attributes such as performance, security, usability, reliability, etc.
- Categorize NFRs using frameworks like ISO/IEC 25010.
- Make them **measurable** (e.g., “System shall respond within 2 seconds”).

### **Step 4: Prioritize and Validate Requirements**
- Use MoSCoW (Must-have, Should-have, Could-have, Won’t-have) or similar.
- Review with stakeholders to ensure alignment.
- Resolve conflicts or ambiguities.

### **Step 5: Document Requirements Clearly**
- Use a Software Requirements Specification (SRS) document.
- Separate FRs and NFRs into distinct sections.
- Include traceability matrices if needed.

### **Step 6: Verify and Test**
- Ensure every requirement has a corresponding test case.
- Functional tests validate behavior; non-functional tests validate quality attributes (e.g., load testing for performance).

### **Step 7: Manage Changes**
- Use change control processes.
- Update documentation and tests when requirements evolve.

---

## **Complete Example: Online Bookstore System**

### **Problem Statement**
A startup wants to build an online bookstore where users can browse books, search by title/author, add items to a cart, place orders, and track deliveries. The system must be secure, fast, and accessible on mobile devices.

---

### **Functional Requirements (FRs)**

1. **User Registration & Login**  
   - FR-01: The system shall allow new users to register using email and password.  
   - FR-02: The system shall authenticate users during login using email and password.

2. **Book Browsing & Search**  
   - FR-03: The system shall display books in categories (e.g., Fiction, Science).  
   - FR-04: The system shall allow users to search books by title, author, or ISBN.  
   - FR-05: The system shall display book details (title, author, price, description, cover image).

3. **Shopping Cart**  
   - FR-06: The system shall allow users to add/remove books to/from a shopping cart.  
   - FR-07: The system shall calculate total price including tax.

4. **Order Management**  
   - FR-08: The system shall allow users to place an order after providing shipping and payment details.  
   - FR-09: The system shall send an order confirmation email upon successful purchase.  
   - FR-10: The system shall allow users to view order history and current status (e.g., “Shipped”, “Delivered”).

5. **Admin Functions**  
   - FR-11: Admins shall be able to add, edit, or remove books from the catalog.  
   - FR-12: Admins shall view all orders and update their status.

---

### **Non-Functional Requirements (NFRs)**

1. **Performance**  
   - NFR-01: The homepage shall load in under 2 seconds on a broadband connection.  
   - NFR-02: The system shall support 1,000 concurrent users without degradation.

2. **Security**  
   - NFR-03: All user passwords shall be stored using bcrypt hashing.  
   - NFR-04: Payment data shall be processed via PCI-DSS compliant third-party gateway (e.g., Stripe).  
   - NFR-05: The system shall enforce HTTPS for all transactions.

3. **Usability**  
   - NFR-06: The interface shall comply with WCAG 2.1 AA accessibility standards.  
   - NFR-07: First-time users shall be able to complete a purchase within 5 minutes without training.

4. **Reliability**  
   - NFR-08: The system shall have 99.9% uptime during business hours (6 AM–12 AM UTC).  
   - NFR-09: Failed transactions shall be logged and recoverable.

5. **Compatibility**  
   - NFR-10: The website shall be fully responsive and functional on Chrome, Firefox, Safari, and Edge (latest two versions).  
   - NFR-11: The mobile interface shall work on iOS 14+ and Android 10+.

6. **Maintainability**  
   - NFR-12: Code shall follow modular design with documented APIs for future feature additions.

7. **Scalability**  
   - NFR-13: The system architecture shall support adding new product categories without code changes.

---

### **Tips for Success**

- **Avoid vague NFRs**: Instead of “The system should be fast,” say “Search results appear within 1 second for 95% of queries.”
- **Link NFRs to business value**: e.g., “High availability ensures no lost sales during peak holiday traffic.”
- **Review early and often**: Involve QA and DevOps teams during requirement definition—they’ll spot testability and deployment issues early.

-
## **1. Introduction to Scrum**

Scrum is an agile framework for developing, delivering, and sustaining complex products. It emphasizes iterative progress, collaboration, and adaptability. Teams work in fixed-length iterations called **Sprints** (typically 2–4 weeks) to deliver potentially shippable product increments.

### **Core Scrum Roles**
| Role | Responsibility |
|------|----------------|
| **Product Owner (PO)** | Maximizes product value; manages the Product Backlog |
| **Scrum Master (SM)** | Facilitates Scrum process; removes impediments; coaches the team |
| **Development Team** | Cross-functional group that delivers working software each Sprint |

### **Scrum Artifacts**
- **Product Backlog**: Ordered list of all features, enhancements, bug fixes, and requirements.
- **Sprint Backlog**: Subset of Product Backlog selected for the current Sprint + plan to deliver it.
- **Increment**: Sum of all completed Product Backlog items at the end of a Sprint—must be “Done” and potentially releasable.

### **Scrum Events**
1. **Sprint** (time-boxed container)
2. **Sprint Planning**
3. **Daily Scrum (Standup)**
4. **Sprint Review**
5. **Sprint Retrospective**

---

## **2. Step-by-Step Scrum Process Using the Online Bookstore Example**

### **Step 1: Create the Product Backlog**

The **Product Owner** gathers requirements (from our earlier FRs/NFRs) and writes them as **user stories** or backlog items, prioritized by business value.

> 📌 **Format**:  
> *As a [type of user], I want [an action] so that [a benefit/a value].*

#### **Sample Product Backlog – Online Bookstore**

| ID | Backlog Item (User Story) | Priority | Est. Effort (Story Points) | Notes |
|----|----------------------------|----------|----------------------------|-------|
| PB-01 | As a new user, I want to register with email and password so I can access my account. | High | 3 | Includes validation & confirmation email |
| PB-02 | As a returning user, I want to log in securely so I can shop. | High | 2 | Must integrate with auth system |
| PB-03 | As a shopper, I want to browse books by category so I can discover titles easily. | High | 5 | Requires category navigation UI |
| PB-04 | As a user, I want to search books by title or author so I can find specific items quickly. | High | 8 | Needs search API + frontend |
| PB-05 | As a customer, I want to add/remove books from my cart so I can manage my order. | High | 5 | Cart must persist across sessions |
| PB-06 | As a buyer, I want to place an order with shipping & payment info so I can complete purchase. | Critical | 13 | Integrates with Stripe; includes email confirmation |
| PB-07 | As a user, I want to view my order history and status so I know when my books arrive. | Medium | 5 | Requires backend order tracking |
| PB-08 | As an admin, I want to add/edit/delete books so I can manage inventory. | Medium | 8 | Admin-only interface |
| PB-09 | As a mobile user, I want the site to work on my phone so I can shop anywhere. | High | N/A | Non-functional – tracked as acceptance criteria |
| PB-10 | As a customer, I want the site to load in under 2 seconds so I don’t abandon my cart. | High | N/A | Performance NFR – verified via testing |

> 💡 **Note**: Non-functional requirements (like PB-09, PB-10) are often included as **acceptance criteria** within relevant user stories or as separate technical enablers.

---

### **Step 2: Sprint Planning (Sprint 1 Example)**

**Goal**: Deliver core shopping experience — registration, login, browsing, and cart.

**Attendees**: PO, SM, Dev Team  
**Duration**: Max 4 hours for a 2-week Sprint

#### **Outcome: Sprint Backlog**

| Selected Items | Tasks (broken down by Dev Team) | Owner | Est. Hours |
|----------------|-------------------------------|-------|-----------|
| PB-01: User Registration | - Design DB schema for users<br>- Build registration form<br>- Implement email confirmation<br>- Write unit tests | Dev A | 12 |
| PB-02: User Login | - Create login API endpoint<br>- Integrate JWT token auth<br>- Add "Forgot Password" flow | Dev B | 10 |
| PB-03: Browse by Category | - Fetch categories from backend<br>- Build responsive category grid<br>- Add hover effects | Dev C | 8 |
| PB-05: Shopping Cart | - Create cart state management<br>- Sync cart with localStorage<br>- Display total price | Dev A & C | 14 |

**Sprint Goal**:  
*"Enable users to sign up, log in, browse books by category, and manage a shopping cart."*

---

### **Step 3: Daily Scrum (Standup Meeting)**

**Time**: Same time daily (e.g., 9:30 AM)  
**Duration**: ≤ 15 minutes  
**Purpose**: Inspect progress toward Sprint Goal and adapt plan

Each team member answers:
1. What did I do yesterday?
2. What will I do today?
3. Are there any impediments?

> ✅ Focus on **collaboration**, not status reporting to the manager.

---

### **Role-Play Script: Daily Standup – Day 3 of Sprint 1**

**Participants**:  
- **Alex** (Scrum Master)  
- **Taylor** (Product Owner)  
- **Jordan** (Frontend Developer)  
- **Morgan** (Backend Developer)  
- **Casey** (Full-Stack Developer)

---

**Alex (Scrum Master)**:  
“Good morning, team! Let’s keep this to 15 minutes. Jordan, you’re up first.”

**Jordan (Frontend)**:  
“Yesterday, I finished the category grid layout and added responsive breakpoints. Today, I’ll connect it to Morgan’s API to fetch real book data. No blockers.”

**Morgan (Backend)**:  
“Yesterday, I completed the `/categories` and `/books` endpoints. I also added rate limiting for security. Today, I’ll start on the user registration API—need to confirm password hashing method with Casey. Minor blocker: waiting on PO to clarify if we need CAPTCHA on signup.”

**Taylor (Product Owner)**:  
“Thanks, Morgan. No CAPTCHA for MVP—just strong validation. We’ll add bot protection later if needed.”

**Morgan**:  
“Got it. Unblock confirmed.”

**Casey (Full-Stack)**:  
“Yesterday, I built the registration form UI and started integrating with backend. Today, I’ll finish form validation and test email confirmation using SendGrid sandbox. Also, I’ll help Morgan with bcrypt setup.”

**Alex**:  
“Great. Any other impediments?”  
*(Team shakes heads)*  
“Alright—let’s pair on the auth integration after standup if needed. Keep focus on the Sprint Goal: functional cart and login by Friday. Thanks, team!”

---

### **Step 4: Sprint Review (End of Sprint)**

**Goal**: Inspect the Increment and adapt Product Backlog.

- Dev Team demonstrates working features:  
  → User registers & logs in  
  → Browses books by category  
  → Adds books to cart  
- PO provides feedback:  
  “Love the cart! But can we add ‘Remove’ button next to each item?” → New backlog item  
- Stakeholders suggest: “Add ‘Wishlist’ feature” → Added to backlog for future prioritization

---

### **Step 5: Sprint Retrospective**

**Goal**: Improve team processes.

**Guiding Questions**:
- What went well?
- What could be improved?
- What will we commit to changing next Sprint?

**Example Outcomes**:
- ✅ **Went well**: Daily pairing reduced bugs
- ❌ **Improvement**: API documentation was delayed
- 🔄 **Action**: Assign doc owner at Sprint Planning next time

---

## **3. Key Alignment with Requirements**

| Requirement Type | How Scrum Handles It |
|------------------|----------------------|
| **Functional (e.g., PB-01, PB-06)** | Captured as user stories in Product Backlog; implemented in Sprints |
| **Non-Functional (e.g., performance, security)** | Included as: <br> • Acceptance criteria (“Site loads <2s”) <br> • Technical enablers (“Set up CDN”) <br> • Definition of Done (“All code scanned for vulnerabilities”) |

> 🔒 **Definition of Done (DoD) Example**:  
> - Code reviewed  
> - Unit & integration tests pass  
> - Performance tested (<2s load)  
> - Deployed to staging  
> - UX validated on mobile

---

## **4. Best Practices**

- **Refine Backlog Continuously**: Hold backlog refinement sessions weekly.
- **Keep Stories Small**: Aim for items completable in 1–3 days.
- **Involve QA Early**: Testers help define acceptance criteria.
- **Make NFRs Visible**: Tag them in Jira or add to DoD checklist.
- **Empower the Team**: Dev Team owns *how* to build; PO owns *what* to build.

---

## **Conclusion**

Scrum turns complex requirements like those for an online bookstore into manageable, value-driven iterations. By maintaining a clear Product Backlog, planning collaboratively, inspecting daily, and adapting relentlessly, teams deliver high-quality software that meets both functional needs and non-functional excellence.


- Example
- Functional & Non-Functional Requirements  
- Scrum framework (Product Backlog, Sprint Planning, Daily Standup, etc.)  
- Realistic problem statement  
- Role-play script for standup  

---

## 🌟 New Example: **"Campus Event Manager" – A University Event Coordination App**

### 🔍 Problem Statement

A mid-sized university struggles with fragmented event announcements. Students miss club meetings, guest lectures, and career fairs because information is scattered across emails, posters, and social media. The university wants a **centralized mobile-first web app** where:
- Student organizations can **create and manage events**
- Students can **browse, RSVP, and receive reminders**
- Admins can **approve events and monitor usage**

The system must be **secure, accessible, and scalable** during peak registration periods.

---

## ✅ Functional & Non-Functional Requirements

### **Functional Requirements (FRs)**

| ID | Requirement |
|----|-----------|
| FR-01 | As a student org leader, I can create an event with title, date, time, location, description, and category (e.g., Academic, Social). |
| FR-02 | As an admin, I must approve new events before they appear publicly. |
| FR-03 | As a student, I can browse upcoming events by date or category. |
| FR-04 | As a user, I can RSVP “Going” or “Not Going” to any approved event. |
| FR-05 | As a user, I receive a browser notification 1 hour before an event I’ve RSVP’d “Going” to. |
| FR-06 | As a user, I can view my RSVP history and upcoming events on a personal dashboard. |
| FR-07 | As an org leader, I can edit or cancel my own events (pending re-approval if edited). |

### **Non-Functional Requirements (NFRs)**

| ID | Requirement |
|----|-----------|
| NFR-01 | **Performance**: Event list loads in ≤1.5 seconds with 500+ concurrent users. |
| NFR-02 | **Security**: Only authenticated students (via university SSO) can access the app. Org leaders can only manage their own events. |
| NFR-03 | **Usability**: WCAG 2.1 AA compliant; usable by students with visual or motor impairments. |
| NFR-04 | **Reliability**: System uptime ≥99.5% during academic term (Sept–May). |
| NFR-05 | **Compatibility**: Works on Chrome, Safari, Firefox, and mobile browsers (iOS/Android). |
| NFR-06 | **Scalability**: Architecture supports adding 10,000+ events per semester without redesign. |
| NFR-07 | **Maintainability**: All API endpoints documented; logging enabled for audit trails. |

---

## 🧩 Scrum Implementation: From Backlog to Standup

### **Product Backlog (Prioritized)**

| ID | User Story | Priority | Est. Points |
|----|----------|--------|------------|
| PB-01 | As a student, I want to log in via university SSO so I don’t need another password. | Critical | 5 |
| PB-02 | As an org leader, I want to submit a new event for approval. | High | 8 |
| PB-03 | As an admin, I want to review and approve/reject pending events. | High | 5 |
| PB-04 | As a student, I want to see a calendar of approved upcoming events. | High | 8 |
| PB-05 | As a user, I want to RSVP to events with one click. | High | 3 |
| PB-06 | As a user, I want push/browser notifications 1 hour before my events. | Medium | 13 |
| PB-07 | As a student, I want a personal dashboard showing my RSVPs and reminders. | Medium | 5 |
| PB-08 | As a developer, I need role-based access control (RBAC) to enforce permissions. | High (Tech Enabler) | 8 |

> 💡 *NFRs like SSO login (NFR-02) and performance (NFR-01) are embedded in acceptance criteria.*

---

### **Sprint 1 Goal**  
*"Enable secure login, event submission, and admin approval workflow."*

**Selected Backlog Items**: PB-01, PB-02, PB-03, PB-08

**Sprint Backlog Tasks**:
- Set up university SSO integration (OAuth 2.0)
- Design event submission form (frontend)
- Build event approval queue (admin UI)
- Implement RBAC middleware
- Write E2E tests for role permissions

---

### 🎭 Role-Play Script: Daily Standup – Day 2 of Sprint 1

**Team**:  
- **Sam** (Scrum Master)  
- **Dr. Lee** (Product Owner – University IT Rep)  
- **Riley** (Frontend Dev)  
- **Dana** (Backend Dev)  
- **Jamie** (DevOps/QA)

---

**Sam (Scrum Master)**:  
“Team, quick huddle—remember, focus on progress toward our Sprint Goal: working auth + event submission. Riley, go ahead.”

**Riley (Frontend)**:  
“Yesterday, I built the event submission form with validation for date/time and category dropdown. Today, I’ll connect it to Dana’s API. No blockers.”

**Dana (Backend)**:  
“Yesterday, I set up the `/events` POST endpoint and started RBAC logic. Today, I’ll finish role checks—org leaders can only POST, admins get GET on `/pending`. Small blocker: waiting on Dr. Lee to confirm if ‘Guest Speaker’ is a valid event category.”

**Dr. Lee (PO)**:  
“Yes, add ‘Guest Speaker’ under Academic. Also, limit event descriptions to 500 characters—students were pasting essays!”

**Dana**:  
“Noted. Unblock confirmed.”

**Jamie (DevOps/QA)**:  
“Yesterday, I configured the test SSO sandbox using the university’s dev IdP. Today, I’ll write Cypress tests for login flow and start performance baseline (checking NFR-01). Also, added logging for all auth attempts—covers NFR-07.”

**Sam**:  
“Excellent. Keep an eye on that 1.5s load target. Any other impediments?”  
*(Silence)*  
“Great. Let’s sync after standup on RBAC edge cases. Stay focused—you’re on track for demo Friday!”

---

### 🔄 End-of-Sprint Outcomes

- **Review**: Team demos SSO login, event submission, and admin approval screen. PO approves.
- **Retrospective Insight**: “We underestimated SSO setup—next time, spike identity integration in refinement.”
- **Backlog Update**:  
  → Add “Character limit: 500” to PB-02 acceptance criteria  
  → New item: “Export event list as iCal” (requested by student council)


