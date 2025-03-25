<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Radio Player</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #222;
            color: white;
            padding: 20px;
        }
        input {
            width: 60%;
            padding: 10px;
            font-size: 16px;
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin-top: 10px;
            cursor: pointer;
        }
        iframe {
            margin-top: 20px;
            width: 80%;
            height: 315px;
        }
    </style>
</head>
<body>
    <h1>Search and Play Music</h1>
    <input type="text" id="searchBox" placeholder="Enter song name...">
    <button onclick="searchSong()">Search</button>
    <div id="player"></div>

    <script>
        function searchSong() {
            let query = document.getElementById("searchBox").value;
            if (query) {
                let embedURL = "https://www.youtube.com/embed?listType=search&list=" + encodeURIComponent(query);
                document.getElementById("player").innerHTML = `<iframe src="${embedURL}" allowfullscreen></iframe>`;
            }
        }
    </script>
</body>
</html>

