### Instructions 

To design an **Online Bookstore System (OBS)**, follow a structured approach that incorporates both functional requirements (FRs) and non-functional requirements (NFRs). Below are detailed instructions to guide you through the process.

https://github.com/hjtejuco123/CS0032-DS/tree/main/FR-NFR-Scrum
---

## **Step 1: Understand the Problem Statement**
- The goal is to create an online bookstore where users can:
  - Browse books by category.
  - Search for books by title, author, or ISBN.
  - Add books to a cart, place orders, and track deliveries.
  - Log in securely and manage their accounts.
  - Receive a seamless experience on mobile devices.
- Admins should be able to manage the catalog and view/update orders.
- The system must meet specific performance, security, usability, reliability, compatibility, maintainability, and scalability requirements.

---

## **Step 2: Analyze Functional Requirements (FRs)**
Carefully review each functional requirement and map out how it will be implemented in your design:

1. **User Registration & Login**
   - Implement a registration form with email and password fields.
   - Use bcrypt hashing (as per NFR-03) to store passwords securely.
   - Authenticate users during login using the stored credentials.

2. **Book Browsing & Search**
   - Display books in predefined categories (e.g., Fiction, Science).
   - Provide a search bar that supports queries by title, author, or ISBN.
   - Show book details such as title, author, price, description, and cover image.

3. **Shopping Cart**
   - Allow users to add/remove books to/from a shopping cart.
   - Calculate the total price, including applicable taxes.

4. **Order Management**
   - Enable users to place orders after entering shipping and payment details.
   - Send an order confirmation email upon successful purchase.
   - Provide a dashboard for users to view their order history and current status.

5. **Admin Functions**
   - Create an admin panel to add, edit, or remove books from the catalog.
   - Allow admins to view all orders and update their statuses.

---

## **Step 3: Evaluate Non-Functional Requirements (NFRs) Using ISO/IEC 25010**
ISO/IEC 25010 provides a framework for evaluating software quality characteristics. Use this standard to ensure your design meets the NFRs effectively.

1. **Performance Efficiency**
   - Ensure the homepage loads in under 2 seconds (NFR-01).
   - Test the system to support 1,000 concurrent users without degradation (NFR-02).

2. **Security**
   - Store user passwords securely using bcrypt hashing (NFR-03).
   - Process payments via a PCI-DSS compliant gateway like Stripe (NFR-04).
   - Enforce HTTPS for all transactions (NFR-05).

3. **Usability**
   - Ensure the interface complies with WCAG 2.1 AA accessibility standards (NFR-06).
   - Conduct usability testing to ensure first-time users can complete a purchase within 5 minutes (NFR-07).

4. **Reliability**
   - Aim for 99.9% uptime during business hours (NFR-08).
   - Log failed transactions and implement recovery mechanisms (NFR-09).

5. **Compatibility**
   - Make the website responsive and functional across Chrome, Firefox, Safari, and Edge (latest two versions) (NFR-10).
   - Ensure the mobile interface works on iOS 14+ and Android 10+ (NFR-11).

6. **Maintainability**
   - Follow modular design principles and document APIs for future feature additions (NFR-12).

7. **Scalability**
   - Design the architecture to support adding new product categories without code changes (NFR-13).

---

## **Step 4: Design the System Architecture**
1. **Frontend**
   - Prepare screen mock design using any wireframe tools	
   - Use a modern frontend framework for building the user interface.
   - Ensure the design is responsive and accessible.

2. **Backend**
   - Use prepared language for the backend logic.


3. **Database**
   - Use a relational database (e.g., PostgreSQL) to store user data, books, and orders.
   - Normalize the database schema to reduce redundancy.

4. **Hosting**
   - Deploy the application on cloud platforms like AWS, Azure, or Google Cloud or any free hosting for scalability and reliability.

---

## **Step 5: Prototype and Test**
1. **Prototype**
   - Build a minimum viable product (MVP) that includes core functionalities such as user registration, book browsing, and order placement.

2. **Testing**
   - Perform unit testing, integration testing, and end-to-end testing.
   - Conduct load testing to ensure the system supports 1,000 concurrent users.
   - Verify compliance with accessibility standards (WCAG 2.1 AA).

---

## **Step 6: Document Your Work**
1. **Requirements Documentation**
   - List all FRs and NFRs in a table format, marking which ones are implemented.

2. **Design Documentation**
   - Include diagrams such as:
     - Entity-Relationship Diagram (ERD) for the database.
     - Sequence diagrams for key workflows (e.g., user registration, order placement).
     - System architecture diagram.

3. **User Manual**
   - Write a simple guide explaining how to use the system for both users and admins.

---

## **Step 7: Present Your Solution**
Prepare a presentation that includes:
- An overview of the problem statement.
- Key features implemented based on FRs and NFRs.
- Screenshots of the prototype.
- Testing results and performance metrics.
- Challenges faced and how they were addressed.

---

**Final Deliverables Checklist:**
- [ ] Functional Requirements Implemented
- [ ] Non-Functional Requirements Evaluated Using ISO/IEC 25010
- [ ] System Architecture Designed
- [ ] Prototype Built and Tested
- [ ] Documentation Prepared
- [ ] Presentation Ready
