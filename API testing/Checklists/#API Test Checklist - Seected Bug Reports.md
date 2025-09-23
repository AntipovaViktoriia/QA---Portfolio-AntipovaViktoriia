# API Test Checklist - Selected Bug Reports

**Environment:** Postman / Swagger (Windows 11 Pro)  
**Module:** Authentication / Registration / Access Token / Room Management  

---

| №  | Section                | Check Item                                             | Expected Result                                  | Status |
|----|------------------------|-------------------------------------------------------|-------------------------------------------------|--------|
| 1  | Registration           | Registration with invalid email                        | 400 Bad Request, refresh token not created     |        |
| 2  | Refresh Token          | Use invalid refresh token                              | 403 Forbidden, appropriate error message       |        |
| 3  | Access Token           | Update access token with valid data                    | 201 OK, new access token received              |        |
| 4  | Room Management        | Create room with `"null"` (string)                    | Room created successfully (201 Created)        |        |
| 5  | Room Management        | Create room with `null` (no quotes)                   | 400 Bad Request, appropriate error message     |        |
| 6  | Registration           | Check username uniqueness                               | `{available: false}` returned, validation shown|        |
