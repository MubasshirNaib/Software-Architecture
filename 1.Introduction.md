# Software Architecture Class Notes
---

## Table of Contents

1. [Introduction to Software Architecture](#introduction-to-software-architecture)
2. [Software Valuation: Assets Versus Liabilities](#software-valuation-assets-versus-liabilities)
3. [Impact on Software Valuation](#impact-on-software-valuation)
4. [Case Study: SundarBan – A Place to Buy and Sell](#case-study-sundarban--a-place-to-buy-and-sell)
5. [API Design and Microservices Communication](#api-design-and-microservices-communication)
6. [Event-Driven Microservices Architecture](#event-driven-microservices-architecture)

---

## Introduction to Software Architecture

- **Definition & Scope:**
  - Software Architecture is the discipline that governs the strategic design, evaluation, and sustainability of software systems.
  - It influences both technical implementation and business outcomes.

---

## Software Valuation: Assets Versus Liabilities

- **Analogy with Financial Balance Sheets:**
  - **Assets:**  
    - Represent aspects like real estate, equipment, cash, investments, and even subscribed customers.
  - **Liabilities:**  
    - Include liabilities such as loans, payables (e.g., salaries), equities, taxes, and employee benefits.
- **Market Examples:**
  - The PDF highlights real-world companies (e.g., WhatsApp, LinkedIn, Slack, Xilinx) along with their acquisition details to illustrate how software companies are valued in the market.
- **Key Comparison:**
  - Just as financial assets and liabilities influence a company's market value, so do technical qualities and shortcomings impact a software product's overall valuation.

---

## Impact on Software Valuation

- **Technical Debt:**
  - **Definition:** Extra work and complications resulting from shortcuts in coding.
  - **Consequences:**
    - Rapid development shortcuts may hinder future growth.
    - Requires future refactoring, thereby slowing down further development.
- **Risk Register:**
  - **Purpose:**  
    - To list potential problems, evaluate their likelihood and impact, and help teams plan to either avoid or mitigate risks.
  - **Best Practices:**
    - The register should be continuously updated as the project evolves.
- **Code Quality:**
  - Directly influences both technical debt and overall project risks.
  - Maintaining high standards of code quality is essential to ensure sustainable project growth and efficiency.

---

## Case Study: SundarBan – A Place to Buy and Sell

- **Overview of the Use Case:**
  - **Business Model:**  
    - An online marketplace named "SundarBan" that facilitates buying and selling.
  - **User Experience:**
    - **Location-Based Products:**  
      - Initially displays products relevant to the user's geographical location.
    - **Personalized Recommendations:**  
      - Shows products based on the user's previous purchase history after logging in.
    - **Search Functionality:**  
      - Enables users to easily search for desired products.
- **Design Challenge:**
  - Define the system modules.
  - Create diagrams to illustrate system workflow.
  - Conceptually identify the databases involved (no detailed table design required).

---

## API Design and Microservices Communication

- **Typical API Endpoints:**
  - `GET /Categories`
  - `GET /product`
  - `POST /checkout`
  - `GET /suggestion`
  - `POST /payment/webhook/bkash`
- **Roles of Endpoints:**
  - **Authentication:**  
    - Read operations to validate user credentials.
  - **Validation:**  
    - Read-only checks to ensure request integrity.
  - **Updates:**  
    - Specific write operations (e.g., payment gateway updates with BKash).
- **Significance:**
  - Illustrates how microservices enable modular functionality via clearly defined API contracts.

---

## Event-Driven Microservices Architecture

- **Communication Model:**
  - Utilizes an event/message bus to enable inter-service communication.
- **Tools & Technologies:**
  - **Event Brokers:**  
    - Examples such as Apache Kafka and RabbitMQ are mentioned for their cloud-agnostic capabilities.
- **Scalability Considerations:**
  - **Hosting:**  
    - Services can be hosted using Elastic Compute solutions along with network/application load balancers.
  - **Future Enhancements:**
    - **Database Sharding:** To distribute load across databases.
    - **CQRS (Command Query Responsibility Segregation):** To optimize read and write operations separately.
