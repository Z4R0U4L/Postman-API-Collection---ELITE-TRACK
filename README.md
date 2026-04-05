# Postman API Collection - TRACK ELITE

This repository contains a Postman collection to test the TRACK ELITE API. It focuses on authentication, role-based registration, and validation scenarios for both merchants and drivers.

---

## 📁 Files Included

- **elite-track-collection.json**: Postman collection with all API requests
- **track-elite-environment.json**: Environment configuration (Base URL, variables)
- **newman-report.html**: Detailed test execution report generated with Newman

---

## ⚙️ How to Use

### 1. Import into Postman
- Open Postman → Import
- Upload:
  - `elite-track-collection.json`
  - `track-elite-environment.json`

---

### 2. Set Environment
- Select **TRACK ELITE**
- Base URL:
```
http://localhost:5000
```

---

### 3. Run Tests
Run inside Postman or using Newman:
```
newman run elite-track-collection.json -e track-elite-environment.json
```

---

## 📊 Test Summary

- Total Requests: 22
- Total Assertions: 51
- Failed Tests: 0 ✅
- Success Rate: 100%

---

## 🔐 All API Tests Included

### 🧑‍💼 Authentication - Merchant

1. Register Merchant - Valid Data  
2. Validate Status Code (201 Created)  
3. Validate Token Returned  
4. Validate Role = Merchant  
5. Validate Response Structure  

---

### 🚚 Authentication - Driver

6. Register Driver - Valid Data  
7. Validate Status Code  
8. Validate Token Returned  
9. Validate Role = Driver  
10. Validate Response Structure  

---

### ⚠️ Error Handling

11. Register with Existing Email  
12. Validate Status Code (409 Conflict)  
13. Validate Error Message  

---

### ✅ Token & Response Validation

14. Token Presence Check  
15. Token Format Validation  
16. Response Contains User Object  
17. Response Contains Required Fields (id, name, email, role, phone)  

---

### 📦 Data Validation

18. Validate Email Format Handling  
19. Validate Password Field Handling  
20. Validate Phone Field Handling  

---

### 🔁 General API Checks

21. Response Time Validation  
22. Multiple Request Stability Test  

---

## 🧪 What is Covered

- ✔️ Successful registration (merchant & driver)  
- ✔️ Duplicate email protection  
- ✔️ JWT authentication validation  
- ✔️ Role-based logic  
- ✔️ API response structure validation  
- ✔️ Error handling scenarios  
- ✔️ Performance checks (response time)  

---

## 🛠️ Tech Stack

- Node.js / Express  
- Postman  
- Newman  

---

## 📌 Notes

- Backend must be running before tests  
- Default Base URL:
```
http://localhost:5000
```

---

## 👨‍💻 Author

Your Name  
https://github.com/Z4R0U4L
