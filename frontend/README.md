## QuickPay

A **MERN** (MongoDB, Express, React, Node.js) based payment application that allows users to sign up, authenticate using JWT, view account balances, and transfer money to other users.

---

### Features

* **User Authentication**: Sign up, sign in, and JWT-based authentication.
* **Account Management**: View current balance, transaction history.
* **Money Transfer**: Securely transfer funds between users.
* **Search Users**: Filter and find other users by name.
* **Protected Routes**: Use JWT to protect sensitive endpoints.

---

### Tech Stack

* **Frontend**: React, Axios, React Router
* **Backend**: Node.js, Express
* **Database**: MongoDB (Atlas)
* **Auth**: JSON Web Tokens (JWT)
* **Styling**: Tailwind CSS

---

### Prerequisites

* Node.js v14+ and npm/yarn
* MongoDB Atlas account (or local MongoDB)
* Git

---

### Getting Started

1. **Clone the repo**:

   ```bash
   git clone https://github.com/yourusername/quickpay.git
   cd quickpay/backend
   ```

2. **Install dependencies**:

   ```bash
   # Backend
   npm install

   # Frontend (in a new tab)
   cd ../frontend
   npm install
   ```

3. **Set up environment variables**:

   * Create a `.env` file in `backend/` with:

     ```env
     PORT=3000
     MONGO_URL="mongodb+srv://<username>:<password>@cluster0.mongodb.net/quickpay?retryWrites=true&w=majority"
     JWT_SECRET=your-secret-key
     ```

4. **Run the application**:

   ```bash
   # Start backend
   cd backend
   npm run dev

   # Start frontend (in separate terminal)
   cd frontend
   npm run dev
   ```

5. **Access the app**:

   * Frontend: [http://localhost:5173](http://localhost:5173)
   * Backend API: [http://localhost:3000/api/v1](http://localhost:3000/api/v1)

---

### API Endpoints

**Auth**

| Method | Endpoint                      | Description                  |
| ------ | ----------------------------- | ---------------------------- |
| POST   | `/api/v1/user/signup`         | Create a new user account    |
| POST   | `/api/v1/user/signin`         | Authenticate and get a token |
| POST   | `/api/v1/user/changePassword` | Change user password         |

**User Search**

| Method | Endpoint                        | Description                     |
| ------ | ------------------------------- | ------------------------------- |
| GET    | `/api/v1/user/bulk?filter=NAME` | Search users by first/last name |

**Account**

*All routes below require a valid JWT in the `Authorization` header.*

| Method | Endpoint                        | Description              |
| ------ | ------------------------------- | ------------------------ |
| GET    | `/api/v1/account/balance`       | Get current user balance |
| POST   | `/api/v1/account/transferMoney` | Transfer money to a user |

---

### Frontend Flow

1. **Signup / Signin**: New users register and receive a JWT upon login.
2. **Dashboard**: View balance and list of users.
3. **Search**: Filter users by name.
4. **Transfer**: Click "Send Money" to open transfer form and complete transactions.

---

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

### Acknowledgments

* [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
* [Express.js](https://expressjs.com/)
* [React](https://reactjs.org/)
* [JWT](https://jwt.io/)
