# Yuxiang-Xie_832301327_Contacts-Web-App_front_end
This is the front-end repository of Web App: Contacts for Assignment 1, EE308

# Contacts Management Web APP----Frontend Part

This is the **frontend** for the **Contacts Management App**, providing a simple user interface to add, edit, delete, and view contacts. It connects to the Django backend API running on port **8000**.

---

## Project Info

- **Frontend Port:** `5500` (e.g., served via Live Server)
- **Backend API URL:** `http://127.0.0.1:8000/contacts/`
- **Frontend URL:** `http://127.0.0.1:5500/Contacts_front_end/index.html`
- **Backend Repository:** (Backend GitHub Link is here: )


## Project Structure

```832301327_contacts_frontend/
├── src/                 # Source code directory
│   ├── index.html       # Main page
│   ├── style.css        # Stylesheet
│   └── script.js        # JavaScript logic for API calls and DOM updates
├── README.md            # Project guidance
├── codestyle.md         # Coding standards
└── LICENSE              # License file```

## How to Run

1. **Ensure Backend is Running**
   - Run the Django backend at [http://127.0.0.1:8000](http://127.0.0.1:8000)
   - Make sure `django-cors-headers` is installed and configured

2. **Open Frontend**
   - Open `index.html` directly, or use a local server:
     - In VS Code → *Right-click* → “Open with Live Server”
     - Or run any static server on port `5500`

3. **Access the App**
   - Go to: [http://127.0.0.1:5500/Contacts_front_end/index.html](http://127.0.0.1:5500/Contacts_front_end/index.html)

---

## Features

- Add new contact (name, email, phone)
- Edit existing contact
- Delete contact
- View all contacts (list fetched from Django API)

---

## API Endpoints Used

| Action | Method | Endpoint |
|---------|---------|-----------|
| Get all contacts | `GET` | `/contacts/` |
| Create contact | `POST` | `/contacts/` |
| Update contact | `PUT` | `/contacts/<id>/` |
| Delete contact | `DELETE` | `/contacts/<id>/` |

---

## Technologies Used

- HTML5, CSS3, JavaScript (ES6)
- Fetch API for HTTP requests
- Django REST Framework backend

---

## Troubleshooting

- **Data doesn’t load:** Check that Django is running on port `8000`
- **CORS error:** Ensure `django-cors-headers` is enabled and `http://127.0.0.1:5500` is in `CORS_ALLOWED_ORIGINS`
- **Port conflict:** Make sure no other app is using port `5500` or `8000`

---

## License

This project is open source under the [MIT License](./LICENSE).
