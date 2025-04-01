# API testing 
## Presentation of my API testing project (CRUD on free API with Tests) in Postman

- **API:** RESTFUL-API [https://restful-api.dev](https://restful-api.dev/)
- **Allowed Methods:** `GET`, `POST`, `PUT`, `PATCH`, `DELETE`, `OPTIONS`, `HEAD`
- **Accepted Objects:** predefined objets `"name"`, `"data"` with free values
- **Base URL:** `https://api.restful-api.dev/`
- **Endpoint:** `/objects`

## Collection Overview and Setting Up Variables

- Postman collection contains CRUD requests grouped in a single folder.
- Variables are created at the collection level to store request (and response) data.

![Collection View](screenshots/PM01.png)


---

## Creating a New Record (POST Request)

- Record data is prepared with random values (`name`, `city`, `address`, `phone`) in **Pre-request Scripts**.

![Pre-req Scripts](screenshots/PM02.png)
 
- Sends a `POST` request with JSON data.
 
![POST Request](screenshots/PM03.png)

- Stores the record `id` from the response in a collection variable.
- Tests response for HTTP status code, header `content-type`, matching `name` & `data`, response time

![POST Request](screenshots/PM04.png)

---

## Updating a Record (PUT Request)

- Modifies the record with a new `address`.
- Stores updated data in a collection variable.

![PUT Request](screenshots/PM05.png)


- Sends `PUT` request with JSON data.

![PUT Request](screenshots/PM06.png)

- Tests response (HTTP status code, header `content-type`, matching `name` & `data`, response time).

![PUT Request](screenshots/PM07.png)

---

## Partial Update (PATCH Request)

- Changes `phone` number and stores updated data in a collection variable.

![PATCH Request](screenshots/PM08.png)

- Updates only the `data` object.

![PATCH Request](screenshots/PM09.png)

- Tests response (HTTP status code, header `content-type`, matching `data`, response time).

![PATCH Request](screenshots/PM10.png)

---

## Retrieving the Record (GET Request)

- Fetches the record to verify updates.

![GET Request](screenshots/PM11.png)

- Tests response (HTTP status code, header `content-type`, matching `name` & `data`, response time).

![GET Request](screenshots/PM12.png)

---

## Deleting a Record (DELETE Request)

- Deletes the created record.

![DELETE Request](screenshots/PM13.png)

- Tests response for HTTP status code, expected message, response time

![DELETE Request](screenshots/PM14.png)

---

## Verifying Deletion (HEAD Request)

- Ensures the record no longer exists using a `HEAD` request.

![HEAD Request](screenshots/PM15.png)

---

## Console log

![Console Log](screenshots/PM16.png)

## Running the Full Collection in Postman Runner

- Executes the entire test collection to validate CRUD operations.

![Collection Run](screenshots/PM17.png)
![Collection Run](screenshots/PM18.png)

---

## 📂 Project Structure
```plaintext
/
├── RESTFULL-API.DEV.postman_collection.json  # Exported Postman collection
├── README.md                                 # Project documentation (this file)
├── screenshots/                              # Folder containing all screenshots
├── docs/                                     # Folder containing project documentation in pdf 
│   ├── Project_Postman.pdf
```

---

## How to Use This Project
1. **Import the Collection**: Open Postman and import `RESTFULL-API.DEV.postman_collection.json`.
2. **Run the Tests**: Execute the collection to validate CRUD operations.
3. **Check the Results**: Review test results and API responses.

---

🚀 Happy Testing! 🎯
