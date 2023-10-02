# InshutiHubV2
This is InshutiHuv Version 2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>InshutiHub</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: powderblue;
        }
        .container {
            max-width: 960px;
            margin: 0 auto;
            padding: 20px;
        }
        .movie-card {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin: 20px 0;
            padding: 20px;
            display: flex;
        }
        .movie-card img {
            max-width: 150px;
            margin-right: 20px;
        }
        .movie-info {
            flex: 1;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>InshutiHub</h1>
        <div class="movie-card" id="movie-list"></div>
    </div>

    <script>
        const movies = [
            {
                title: "Movie 1",
                image: "https://via.placeholder.com/150",
                description: "Description of Movie 1."
            },
            {
                title: "Movie 2",
                image: "https://via.placeholder.com/150",
                description: "Description of Movie 2."
            },
            {
                title: "Movie 3",
                image: "https://via.placeholder.com/150",
                description: "Description of Movie 3."
            }
        ];

        const movieList = document.getElementById("movie-list");

        movies.forEach(movie => {
            const movieCard = document.createElement("div");
            movieCard.className = "movie-card";

            const image = document.createElement("img");
            image.src = movie.image;
            movieCard.appendChild(image);

            const movieInfo = document.createElement("div");
            movieInfo.className = "movie-info";

            const title = document.createElement("h2");
            title.textContent = movie.title;
            movieInfo.appendChild(title);

            const description = document.createElement("p");
            description.textContent = movie.description;
            movieInfo.appendChild(description);

            movieCard.appendChild(movieInfo);

            movieList.appendChild(movieCard);
        });
    </script>
</body>
</html>
