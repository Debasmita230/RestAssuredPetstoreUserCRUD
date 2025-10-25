# RestAssured Petstore User CRUD Automation

# Objective:
Practice REST API testing using **Java + RestAssured + TestNG** by performing CRUD operations on the Swagger Petstore `/user` endpoint.


# Project Structure:

RestAssuredPetstoreUserCRUD/
├── pom.xml
├── README.md
├── src/
│   ├── main/java/com/api/testing/
│   │   └── RestAssuredPetstoreUserCRUD.java
│   │
│   └── test/java/
│       ├── com/api/tests/UserCRUDTest.java
│       └── com/api/utils/BaseTest.java
├── target/
└── test-output/

# Explanation:
 BaseTest.java` → sets base URI for API calls.  
 UserCRUDTest.java` → contains all CRUD test cases.  
 pom.xml` → Maven dependency management.  
 README.md` → project overview and execution guide.



# Features Implemented:
✅ Create user using POST /user 
✅ Fetch user details using GET /user/{username}  
✅ Update user using PUT /user/{username}  
✅ Delete user using DELETE /user/{username}

Each test includes:
- Proper JSON request body creation.
- Response validation using assertions.
- Short waits and retry logic to handle Petstore API latency.
- Dynamic username (System.currentTimeMillis()) to avoid collisions.

---

# How to Run Tests:

# Option 1 — From Eclipse
1. Open the project in Eclipse.  
2. Right-click on testng.xml→ Run As → TestNG Suite.

# Option 2 — From Command Line
   bash
   mvn test

# Test Result:

PASSED: testCreateUser
PASSED: testGetUser
PASSED: testUpdateUser
PASSED: testDeleteUser


