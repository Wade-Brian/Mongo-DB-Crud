# 🧩 MongoDB CRUD Checkpoint

This project demonstrates the basic **MongoDB CRUD operations** (Create, Read, Update, Delete) using a simple contact list example.  
It was completed as part of a database learning checkpoint to show how to manipulate data in MongoDB.

---

## 📘 Project Overview

- **Database name:** `contact`
- **Collection name:** `contactlist`

The database stores a list of contact documents, each with the following fields:
- `last_name`
- `first_name`
- `email` (optional)
- `age`

---

## 🧠 Operations Performed

### 1️⃣ Insert Multiple Documents
Added the following sample data into the `contactlist` collection:
| Last Name | First Name | Email | Age |
|------------|-------------|-------|-----|
| Ben | Moris | ben@gmail.com | 26 |
| Kefi | Seif | kefi@gmail.com | 15 |
| Emilie | Brouge | emilie.b@gmail.com | 40 |
| Alex | Brown | — | 4 |
| Denzel | Washington | — | 3 |

---

### 2️⃣ Display All Contacts
Command:
```js
db.contactlist.find()
Displays all the documents stored in the collection.

3️⃣ Display One Contact by ID
Command:

js
Copy code
db.contactlist.findOne({ _id: ObjectId("your_id_here") })
Shows all the information about one specific contact using their MongoDB ID.

4️⃣ Display Contacts with Age > 18
Command:

js
Copy code
db.contactlist.find({ age: { $gt: 18 } })
5️⃣ Display Contacts with Age > 18 and Name Containing "ah"
Command:

js
Copy code
db.contactlist.find({ 
  age: { $gt: 18 }, 
  first_name: { $regex: /ah/i } 
})
6️⃣ Update Contact’s First Name
Change “Kefi Seif” to “Kefi Anis”:

js
Copy code
db.contactlist.updateOne(
  { first_name: "Seif", last_name: "Kefi" },
  { $set: { first_name: "Anis" } }
)
7️⃣ Delete Contacts Aged Under 5
Command:

js
Copy code
db.contactlist.deleteMany({ age: { $lt: 5 } })
8️⃣ Display Final Contact List
After deletions, confirm the remaining contacts:

js
Copy code
db.contactlist.find()
🖼️ Screenshots
All screenshots showing the commands and outputs are available inside the /screenshots folder:

Insert documents

Display all contacts

Find one by ID

Age > 18

Age > 18 & name contains “ah”

Update record

Delete under age 5

Final list

⚙️ Tools Used
MongoDB Compass / MongoDB Playground (for database operations)

Git & GitHub (for version control)

VS Code / Cursor (for editing and documentation)

🧾 Author
Name: Brian Okech Wade
Project: MongoDB CRUD Checkpoint
Date: November 2025
