# CRUD-API-and-JSON

# Song API

This project implements a simple Song API using Flask. It allows users to retrieve songs, add new songs, update existing songs, and delete songs.

## Installation

1. Clone the repository:
   cmd
   git clone https://github.com/EronRei/CRUD-API-and-JSON

2. Navigate to the project directory

3. Install the required dependencies:
pip install -r requirements.txt

4. Start the server:
python song.py


# USAGE

# GET /songs

Response:

{
  "songs": [
    {
      "Title": "Rise Up",
      "Artist": "Andra Day",
      "Genre": "Pop",
      "ID": 123123,
      "Release": 2016
    },
    {
      "Title": "Bohemian Rhapsody",
      "Artist": "Queen",
      "Genre": "Rock",
      "ID": 123124,
      "Release": 1975
    },
    ...
  ]
}

# Get a specific song

GET /songs/123123

Response:
{
  "Title": "Rise Up",
  "Artist": "Andra Day",
  "Genre": "Pop",
  "ID": 123123,
  "Release": 2016
}

# Add a new song

Request:
POST /songs
Content-Type: application/json

{
  "Title": "New Song",
  "Artist": "New Artist",
  "Genre": "Pop",
  "ID": 123128,
  "Release": 2021
}
Response:
{
  "message": "Song created successfully."
}

# Update a song

Request:    
PUT /songs/123128
Content-Type: application/json

{
  "Title": "Updated Song",
  "Artist": "Updated Artist",
  "Genre": "Pop",
  "ID": 123128,
  "Release": 2022
}
Response:
{
  "message": "Song created successfully."
}


# Update a song
Send a PUT request to /songs/{ID} to update an existing song by its ID.

Request:
PUT /songs/123128
Content-Type: application/json

{
  "Title": "Updated Song",
  "Artist": "Updated Artist",
  "Genre": "Pop",
  "ID": 123128,
  "Release": 2022
}

Response:
{
  "message": "Song updated successfully."
}
 
# Delete a song
Request:
DELETE /songs/123128

Response:
{
  "message": "Song deleted successfully."
}