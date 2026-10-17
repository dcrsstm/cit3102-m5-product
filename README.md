cit3102-m5-product

Hello, Sir Kurt! I completed the activity individually because I'm currently sick for a week due to my allergies and had difficulty coordinating with a partner. I understand that this activity was supposed to be done in pairs, and I sincerely apologize for not following that instruction. I also want to be honest that I used AI as a guide to help me understand and complete the activity. I still did my best despite not feeling well, and I hope for your kind understanding and consideration. Thank you po

Project Title: Laravel Product API

Member: Danille Christian F. Crisostomo

Section: IT3E

Resource: Product

Setup Steps
1. Clone the repository and navigate to the project folder:
- git clone https://github.com/your-username/cit3102-m5-product.git
- cd cit3102-m5-product

2. Install PHP dependencies:
- composer install

3. Copy the environment configuration file:
- copy .env.example .env

4. Generate the application key:
- php artisan key:generate

5. Run the database migrations:
- php artisan migrate

6. Start the local development server:
- php artisan serve

Routes Table
| HTTP Verb | Path | Description | Requires Token? |
| :--- | :--- | :--- | :--- |
| POST | /api/register | Register a new user | No |
| POST | /api/login | Log in an existing user | No |
| POST | /api/logout | Log out and revoke token | Yes |
| GET | /api/me | Get authenticated user | Yes |
| GET | /api/products | List all products | Yes |
| POST | /api/products | Create a new product | Yes |
| GET | /api/products/{id} | Show a single product | Yes |
| PUT | /api/products/{id} | Update a product | Yes |
| DELETE | /api/products/{id} | Delete a product | Yes |

Screenshots

1. POST /api/register (201 Created)
<img width="1158" height="750" alt="image" src="https://github.com/user-attachments/assets/a33ce3d2-5a0c-46d9-8a3b-1280b115c81e" />

2. POST /api/login (200 OK)
<img width="1155" height="750" alt="image" src="https://github.com/user-attachments/assets/7263e9ef-f8d8-4364-af7e-0d7c13c3927e" />

3. GET /api/products without token (401 Unauthorized)
<img width="1158" height="745" alt="image" src="https://github.com/user-attachments/assets/9958c398-c750-4380-be39-e26e84ead8df" />

4. GET /api/products with token (200 OK)
<img width="1158" height="743" alt="image" src="https://github.com/user-attachments/assets/8a7d1d6d-4bd9-45e7-b328-e43d5058db26" />

5. POST /api/products valid data (201 Created)
<img width="1159" height="743" alt="image" src="https://github.com/user-attachments/assets/8d0746e1-bbdd-487a-988d-5d896b203ae8" />

6. POST /api/products missing fields (422 Unprocessable Entity)
<img width="1156" height="744" alt="image" src="https://github.com/user-attachments/assets/cf20da0f-0c21-4d05-b2e8-787019a97900" />

7. GET /api/products/{id} (200 OK)
<img width="1157" height="740" alt="image" src="https://github.com/user-attachments/assets/9ed285ac-940d-4c6e-8ca7-48a680b397b1" />

8. GET /api/products/{id} not found (404 Not Found)
<img width="1160" height="746" alt="image" src="https://github.com/user-attachments/assets/83fa4fcb-a7db-4daf-b604-40e8a1da0368" />

9. PUT /api/products/{id} (200 OK)
<img width="1157" height="735" alt="image" src="https://github.com/user-attachments/assets/24e86dff-80d6-4ee3-a348-516b01c56af8" />

10. DELETE /api/products/{id} (204 No Content)
<img width="1156" height="744" alt="image" src="https://github.com/user-attachments/assets/e597915a-695f-4cc9-98ca-a177a5d38e66" />



Explanation: Why does DELETE return 204 and not 200?

The HTTP 204 No Content status code means the server successfully processed a request. It intentionally returns an empty response body because there is no extra data to send back. This status is commonly used when a resource has been successfully deleted. Returning an empty body with this status code is standard practice for REST APIs.
