# History Microservice

The History Microservice is a Node.js application that records the username, video path, and timestamp when a user views a video. It provides an API for adding/viewing video history.

## Prerequisites

- Node.js and npm should be installed on your machine.
- MongoDB database should be available with the required credentials. Set the database host and name using the environment variables DBHOST and DBNAME.

## Installation

1. Clone the repository:

   \`\`\`
   git clone https://github.com/your-username/history-microservice.git
   \`\`\`

2. Navigate to the project directory:

   \`\`\`
   cd history-microservice
   \`\`\`

3. Install the dependencies:

   \`\`\`
   npm install
   \`\`\`

4. Set the environment variables:
   - DBHOST: Specify the database host where MongoDB is running.
   - DBNAME: Specify the name of the MongoDB database.

5. Start the microservice:

   \`\`\`
   npm start
   \`\`\`

   The microservice will start running on the specified port (default: 30010).

## API Endpoints

### POST /video

Adds a video to the history collection.

#### Request Body

\`\`\`
{
  "videoPath": "madhuban.mp4",
  "username": "Aakash"
}
\`\`\`

#### Response

- 200 OK: Video added successfully.
- 500 Internal Server Error: Failed to add video to history.

### GET /history

Retrieves video history from the database.

#### Query Parameters

- skip: Number of records to skip (optional).
- limit: Maximum number of records to retrieve (optional).

#### Response

- 200 OK: Returns the video history as a JSON array.
- 500 Internal Server Error: Failed to retrieve video history.
