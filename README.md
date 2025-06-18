# API Testing Portfolio with Postman

Ini adalah project portofolio pengujian API menggunakan **Postman** yang saya buat sebagai bagian dari demonstrasi keterampilan saya di bidang Software Quality Assurance (SQA). Saya menggunakan **dummy API dari [reqres.in](https://reqres.in)** untuk mensimulasikan proses testing seperti login, membuat user, dan pengambilan data user.

---

## 🚀 Tools yang Digunakan

- ✅ Postman (Manual & Automated Testing)
- ✅ JSON & JavaScript Test Scripts

---

## 📂 Struktur Project


---

## 📌 Daftar Test Case

| No | Test Case                         | Method | Endpoint               | Expected Result       |
|----|-----------------------------------|--------|------------------------|------------------------|
| 1  | Login (Success)                   | POST   | /api/login             | Status 200 + Token     |
| 2  | Login (Missing Password)          | POST   | /api/login             | Status 400 + Error     |
| 3  | Get Single User                   | GET    | /api/users/2           | Status 200 + User Data |
| 4  | Create User                       | POST   | /api/users             | Status 201 + User Info |

---

## 📜 Contoh Test Script

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Token should be returned", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData.token).to.be.a("string");
});
