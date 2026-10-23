# IMovies - Movie Ticket Booking (MERN starter)

A beginner-friendly full-stack project using React (Vite), Node.js, Express and MongoDB.
The app can also run in demo mode without MongoDB; demo bookings are stored in server memory and reset when the server restarts.

## Requirements
- Node.js LTS and npm: https://nodejs.org/en/download
- Visual Studio Code: https://code.visualstudio.com/download
- Optional database: MongoDB Atlas free cluster: https://www.mongodb.com/docs/atlas/tutorial/deploy-free-tier-cluster/

## 1. Open the project
Extract this ZIP. In VS Code, choose **File > Open Folder** and open the `IMovies-Movie-Ticket-Booking` folder.

## 2. Install dependencies
Open **Terminal > New Terminal** in VS Code, make sure the terminal is in the project root (the folder containing this README), then run:

```bash
npm install
npm run install-all
```

## 3. Start the app
In the same terminal, run:

```bash
npm run dev
```

Open the frontend at http://localhost:5173
Backend health check: http://localhost:5000/api/health

Keep the terminal running while using the app. Press Ctrl+C to stop both servers.

## 4. Connect MongoDB (optional, for persistent bookings)
1. Create a free MongoDB Atlas cluster and a database user.
2. In Atlas, add your current IP to Network Access and select **Connect > Drivers** to copy the connection string.
3. Copy `server/.env.example` to `server/.env`.
4. Replace the example `MONGO_URI` with your own connection string. Replace `<db_password>` with the database user's password and encode special characters if necessary.
5. Restart the app. The server console should say it connected to MongoDB.

Never share your database password or upload `server/.env` to GitHub. `.env` is ignored by Git.

## Features in this starter
- Movie listing with sample movies
- Select movie, showtime and seats
- Calculate booking total
- Create a booking through the Express API
- Show booking confirmation
- MongoDB persistence when `MONGO_URI` is configured; demo-memory mode otherwise

## Common issues
- `node is not recognized`: install Node.js LTS, then close and reopen VS Code.
- Port already in use: close the other server using that port, or change the port in `server/index.js` / `client/vite.config.js`.
- MongoDB connection error: check the URI, database username/password, and Atlas IP access list. The app can still run in demo mode without MongoDB.
- If npm installation fails, confirm your internet connection and run the command again.

This is a learning project starter. Before public deployment, add proper authentication, payment-provider integration, input validation, rate limiting and production security settings. Do not collect real payment details in this demo.
