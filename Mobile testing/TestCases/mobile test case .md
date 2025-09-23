# 🧪 Test Cases – Mobile Registration

**TC-MOB-001** – Successful registration with valid data  
**Steps**:  
1. Open app.  
2. Open registration form.  
3. Fill in Email: `test@example.com`.  
4. Fill in Username: `user123`.  
5. Fill in Password: `Test1234`.  
6. Repeat Password: `Test1234`.  
7. Tap **Continue**.  
**Expected result**: Message *“Registration successful”* appears.  

**TC-MOB-002** – Continue button becomes active after filling all fields  
**Steps**:  
1. Open app.  
2. Fill in all required fields with valid data.  
**Expected result**: **Continue** button becomes active.  

---

## ❌ Negative Test Cases

**TC-MOB-003** – Invalid email format  
**Steps**:  
1. Open registration form.  
2. Enter Email: `user@`.  
3. Fill other fields validly.  
4. Tap **Continue**.  
**Expected result**: Error *“Invalid email”*.  

**TC-MOB-004** – Passwords do not match  
**Steps**:  
1. Open registration form.  
2. Fill in Password: `Test1234`.  
3. Fill in Repeat password: `Wrong123`.  
4. Tap **Continue**.  
**Expected result**: Error *“Passwords do not match”*.  

**TC-MOB-005** – Existing email  
**Steps**:  
1. Open registration form.  
2. Enter already registered Email.  
3. Fill other fields validly.  
4. Tap **Continue**.  
**Expected result**: Error *“This email is already registered”*.  

**TC-MOB-006** – Empty fields  
**Steps**:  
1. Open registration form.  
2. Tap **Continue** without filling fields.  
**Expected result**: Fields are highlighted red + error “Field is required”.  