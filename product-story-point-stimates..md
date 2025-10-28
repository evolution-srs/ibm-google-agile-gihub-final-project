## Product Catalog Story Point Estimates and Prioritization 

### Product Catalog User Story Backlog
The points stossy assigned based on the Fibonacci sequence (1, 2, 3, 5, 8, 13...), which is common in Scrum, using relative sizing for a typical, moderately experienced team building a basic RESTful API.

The complexity is primarily driven by database interactions, API endpoint creation, and integration with external systems (like the cloud/CI/CD).
### ⭐️ Story Point Estimates and Rationale

| # | User Story Title | Primary Focus | Estimated Story Points | Rationale |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Create a Product | CRUD (Create), Data Validation | 3 | Basic API endpoint, simple database write, but complexity increases slightly due to the required **data validation** logic. |
| 2 | Retrieve a Product | CRUD (Read), Single Fetch | 1 | The **simplest operation**. Basic API endpoint to fetch a single record from the database by a unique ID. |
| 3 | Update a Product | CRUD (Update), Data Validation | 3 | Requires fetching the existing record first for comparison, applying validation, and then performing the write-back operation. |
| 4 | Delete a Product | CRUD (Delete), Dependency Checks | 2 | Basic API endpoint and database delete. Considers potential **foreign key dependency checks**. |
| 5 | Like a Product | Interaction, Counter Update | 3 | Requires validation (user logged in/not liked yet), and an **atomic increment operation** in the database. |
| 6 | Dislike a Product | Interaction, Counter Update | 3 | Same complexity as "Like," needing similar validation logic and an **atomic database update**. |
| 7 | List All Products | CRUD (Read), Pagination/Sorting | 5 | More complex retrieval. Requires a flexible API endpoint, efficient database querying, **mandatory pagination logic**, and default sorting. |
| 8 | Query a Subset of Products | Advanced Search/Filter | 8 | The most complex data retrieval. Requires building **dynamic database queries** based on multiple optional user criteria. |
| 9 | Cloud Hosting | Technical Setup (Infra) | 5 | Initial setup of core cloud resources and configuration for a **single, secure environment**. |
| 10 | Automated Deployment | Technical Setup (CI/CD) | 8 | Setting up a **robust, end-to-end CI/CD pipeline** (GitHub integration, build, test, and automated deployment). |

---

### 🔝 User Story Prioritization for MVP
The prioritization scale, often applied by Product Owners:

* P1 (Must Have): Core functionality; the Minimum Viable Product (MVP) cannot launch without it.

* P2 (Should Have): Important features that deliver high value, but the MVP can function without them temporarily.

* P3 (Could Have): Nice-to-have features; low impact if omitted early on.

* P4 (Won't Have/Defer): Features that are low priority or will be pushed to later releases.

| # | User Story Title | Story Points | Assigned Priority | Justification |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Create a Product | 3 | **P1 (Must Have)** | Core backend function. You can't have a catalog without the ability to add products. |
| 2 | Retrieve a Product | 1 | **P1 (Must Have)** | Core backend function. Products must be fetchable and displayable. |
| 3 | Update a Product | 3 | **P2 (Should Have)** | Essential for business operations, but immediate need can be temporarily mitigated. |
| 4 | Delete a Product | 2 | **P2 (Should Have)** | Necessary, but can be managed by marking products as "Inactive" initially. |
| 5 | Like a Product | 3 | **P3 (Could Have)** | A **value-add feature** for customer engagement; not critical for initial sales functionality. |
| 6 | Dislike a Product | 3 | **P3 (Could Have)** | Similar to 'Like', an engagement/feedback feature that can be deferred. |
| 7 | List All Products | 5 | **P1 (Must Have)** | **Critical for store front.** Required to show the customer a browsable catalog homepage. |
| 8 | Query a Subset of Products | 8 | **P2 (Should Have)** | Crucial for good UX, but basic browsing covers the MVP. **Highest priority P2.** |
| 9 | Cloud Hosting | 5 | **P1 (Must Have)** | **Non-negotiable infrastructure requirement** based on stakeholder needs. |
| 10 | Automated Deployment | 8 | **P2 (Should Have)** | Vital for speed and quality, but the first few deployments can be manual. **Highest priority technical enabler.** |
