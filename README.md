# API testing 
## Presentation of my API testing project (CRUD on free API with Tests) in Postman

- **API:** [RESTFUL-API](https://restful-api.dev/)
- **Allowed Methods:** `GET`, `POST`, `PUT`, `PATCH`, `DELETE`, `OPTIONS`, `HEAD`
- **Accepted Objects:** `"name"`, `"data"` (with free values)
- **Base URL:** `https://api.restful-api.dev/`
- **Endpoint:** `/objects`

## 📁 Collection Overview

Postman collection contains CRUD requests grouped in a single folder.

![Collection View](screenshots/collection_view.png)

---

## 🛠️ Setting Up Variables

- Variables are created at the collection level to store request data.
- Record data is prepared with random values (`name`, `city`, `address`, `phone`) in **Pre-request Scripts**.

![Variables Setup](screenshots/variables_setup.png)

---

## 📌 Creating a New Record (POST Request)

- Sends a `POST` request with JSON data.
- Stores the `record id` from the response in a collection variable.
- Tests response for:
  - HTTP status code
  - Header `content-type`
  - Matching `name` & `data`
  - Response time

![POST Request](screenshots/post_request.png)

---

## 🔄 Updating a Record (PUT Request)

- Modifies the record with a new `address`.
- Stores updated data in a collection variable.
- Tests response for correctness.

![PUT Request](screenshots/put_request.png)

---

## 🔄 Partial Update (PATCH Request)

- Updates only the `data` object (e.g., changes `phone` number).
- Stores updated data in a collection variable.
- Tests response for correctness.

![PATCH Request](screenshots/patch_request.png)

---

## 🔍 Retrieving the Record (GET Request)

- Fetches the record to verify updates.
- Tests response for correctness.

![GET Request](screenshots/get_request.png)

---

## ❌ Deleting a Record (DELETE Request)

- Deletes the created record.
- Tests response for:
  - HTTP status code
  - Expected message
  - Response time

![DELETE Request](screenshots/delete_request.png)

---

## ✅ Verifying Deletion (HEAD Request)

- Ensures the record no longer exists using a `HEAD` request.

![HEAD Request](screenshots/head_request.png)

---

## 🏁 Running the Full Collection

- Executes the entire test collection to validate CRUD operations.

![Collection Run](screenshots/collection_run.png)

---

## 📂 Project Structure
```plaintext
/
├── Postman_Collection.json  # Exported Postman collection
├── README.md                # Project documentation (this file)
├── screenshots/             # Folder containing all screenshots
│   ├── collection_view.png
│   ├── variables_setup.png
│   ├── post_request.png
│   ├── put_request.png
│   ├── patch_request.png
│   ├── get_request.png
│   ├── delete_request.png
│   ├── head_request.png
│   ├── collection_run.png
```

---

## 📌 How to Use This Project
1. **Import the Collection**: Open Postman and import `Postman_Collection.json`.
2. **Run the Tests**: Execute the collection to validate CRUD operations.
3. **Check the Results**: Review test results and API responses.

---

🚀 Happy Testing! 🎯
