# API Test Cases - Selected Bug Reports

**Environment:** Postman / Swagger (Windows 11 Pro)  
**Module:** Authentication / Registration / Access Token / Room Management  

---

## Test Case for BR-085 - Refresh token created on failed registration

| №  | Action / Step                                      | Expected Result                                   | Status |
|----|----------------------------------------------------|--------------------------------------------------|--------|
| 1  | Open Postman                                      | Postman is ready to execute requests            |        |
| 2  | Execute POST request to `/sign-up` with invalid email | Server returns 400 Bad Request                  |        |
| 3  | Check Cookies tab in Postman                       | Refresh token is **not created**                |        |

---

## Test Case for BR-092 - Invalid refresh token causes 500 instead of 403

| №  | Action / Step                                             | Expected Result                                | Status |
|----|-----------------------------------------------------------|-----------------------------------------------|--------|
| 1  | Open Postman                                            | Postman ready                                 |        |
| 2  | Send POST request to `/refresh-token` with invalid token | Server returns 403 Forbidden                  |        |
| 3  | Check response body                                      | Error message displayed correctly             |        |

---

## Test Case for BR-108 - Error updating access token

| №  | Action / Step                                                | Expected Result                                    | Status |
|----|--------------------------------------------------------------|---------------------------------------------------|--------|
| 1  | Open Swagger and Postman                                     | Ready to execute requests                          |        |
| 2  | Send POST request to `/refresh-token` with valid data       | Server returns 201 OK                              |        |
| 3  | Verify response                                             | New access token received successfully            |        |

---

## Test Case for BR-147 - Incorrect handling of null in name field

| №  | Action / Step                                                      | Expected Result                                     | Status |
|----|--------------------------------------------------------------------|---------------------------------------------------|--------|
| 1  | Sign in as admin in Swagger UI                                      | Admin access granted                              |        |
| 2  | Create room with name `"null"` (in quotes)                          | Room created successfully (201 Created)          |        |
| 3  | Create another room with `name: null` (without quotes)             | Server returns 400 Bad Request                    |        |

---

## Test Case for BR-154 - Incorrect check of username uniqueness

| №  | Action / Step                                         | Expected Result                                       | Status |
|----|-------------------------------------------------------|-----------------------------------------------------|--------|
| 1  | Open registration form                                | Form ready                                          |        |
| 2  | Enter a username that already exists (e.g., Testermeta) | Server returns `{available: false}`                 |        |
| 3  | Check validation                                      | Validation message appears, Continue button disabled |        |
