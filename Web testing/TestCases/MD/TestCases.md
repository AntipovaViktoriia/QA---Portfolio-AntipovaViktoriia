# Web Testing Test Cases

## ✅ Registration

### TC-001: Open registration form
**Precondition:** User is on the main page  
**Steps:**
1. Click the "Sign up" button  
**Expected Result:** Registration form opens  

---

### TC-002: Close registration form via [X]
**Precondition:** Registration form is open  
**Steps:**
1. Click the "X" button in the top right corner  
**Expected Result:** Registration form is closed  

---

### TC-003: Close registration form via overlay
**Precondition:** Registration form is open  
**Steps:**
1. Click outside the registration form (on the overlay)  
**Expected Result:** Registration form is closed  

---

### TC-004: Email validation
**Precondition:** Registration form is open  
**Steps:**
1. Enter invalid email (test@)  
**Expected Result:** Error message “Invalid email” is shown immediately  

---

### TC-005: Password match
**Precondition:** Registration form is open  
**Steps:**
1. Enter Password = "123456"  
2. Enter Repeat Password = "1234567"  
**Expected Result:** Error message “Password must be at least 8 characters”  

---

### TC-006: Step progress bar
**Precondition:** Registration form is open  
**Steps:**
1. Fill out the first step of registration  
2. Proceed to the next step  
**Expected Result:** Step progress bar highlights the correct step  

---

## ✅ Login

### TC-007: Open login form
**Precondition:** User is on the main page  
**Steps:**
1. Click the "Login" button  
**Expected Result:** Login form opens  

---

### TC-008: Email validation
**Precondition:** Login form is open  
**Steps:**
1. Enter invalid email (user@)  
**Expected Result:** Error message “Invalid email”  

---

### TC-009: Wrong credentials
**Precondition:** Login form is open  
**Steps:**
1. Enter valid email but invalid password  
2. Click “Login”  
**Expected Result:** Error message “Incorrect email or password”  

---

### TC-010: “Sign up” link in login form
**Precondition:** Login form is open  
**Steps:**
1. Click on the “Sign up” link  
**Expected Result:** Registration form opens  

---

### TC-011: Successful login
**Precondition:** Valid user is registered  
**Steps:**
1. Enter correct email and password  
2. Click “Login”  
**Expected Result:** User is redirected to their home page  
