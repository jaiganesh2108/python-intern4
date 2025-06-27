# Flask REST API – User Management

This project is a simple REST API built using **Flask** to manage user data. It supports basic CRUD operations: **Create, Read, Update, and Delete**.

---

## Tech Stack

- Python 3
- Flask
- PowerShell (for testing the API)
- Optional: curl / Postman

---

## How to Run the App

1. Clone or download the repo
2. Install Flask:
   ```bash
   pip install Flask
   python app.py
   ```
## How to Use with PowerShell
Create a User (POST):
-powershell
-Copy
-Edit

## Get All Users (GET):
```bash
Invoke-RestMethod -Uri "http://127.0.0.1:5000/users" -Method GET
```
Get a User by ID (GET):
```bash
Invoke-RestMethod -Uri "http://127.0.0.1:5000/users/1" -Method GET
```
Update a User (PUT):
```bash
Invoke-RestMethod -Uri "http://127.0.0.1:5000/users/1" `
  -Method PUT `
  -Headers @{ "Content-Type" = "application/json" } `
  -Body '{ "name": "Alice Smith" }'
```
Delete a User (DELETE):
```bash
Invoke-RestMethod -Uri "http://127.0.0.1:5000/users/1" -Method DELETE
```
Sample JSON Format:
```bash
{
  "id": 1,
  "name": "Alice",
  "email": "alice@example.com"
}
```
Data Storage:
-This project uses an in-memory Python dictionary.
-Data will be lost when the server stops
-You can extend it to use SQLite, MongoDB, or any database of your choice.
