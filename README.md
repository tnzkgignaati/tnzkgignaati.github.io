<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Image Caption</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 2rem;
            margin: 0;
            gap: 2rem;
        }

        .image-container {
            position: relative;
            width: 1024px;
            height: 1024px;
            overflow: hidden;
            border-radius: 1rem;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }

        .image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover; /* Ensures the image covers the container without distortion */
            display: block;
        }

        .image-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.8) 0%, rgba(0, 0, 0, 0) 100%);
            color: white;
            padding: 3rem 1.5rem 1.5rem;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            transition: opacity 0.3s ease-in-out;
        }

        .caption-title {
            font-size: 4rem; /* Adjusted for 1024x1024 resolution */
            font-weight: 700;
            color: #00ff00;
            line-height: 1.2;
            text-transform: uppercase;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }

        .caption-text {
            font-size: 2rem; /* Adjusted for 1024x1024 resolution */
            font-weight: 400;
            line-height: 1.5;
            text-align: center;
            max-width: 90%;
            margin-top: 1rem;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.7);
        }

        /* Responsive adjustments for smaller screens */
        @media (max-width: 1024px) {
            .image-container {
                width: 100%;
                height: auto;
            }
            .caption-title {
                font-size: 2.5rem;
            }
            .caption-text {
                font-size: 1.25rem;
            }
        }
    </style>
</head>
<body>

    <div class="image-container">
        <!-- The image to display -->
        <img id="main-image" src="https://oaidalleapiprodscus.blob.core.windows.net/private/org-qkmJQuJ2WnvoIKMr2UJwIJkZ/user-aNsDaZ8exL3uSlpKcTv3KBRo/img-gq0VnifBC5z8okVRejuXi3HY.png?st=2025-09-12T09%3A24%3A27Z&se=2025-09-12T11%3A24%3A27Z&sp=r&sv=2024-08-04&sr=b&rscd=inline&rsct=image/png&skoid=8c7ba6b3-5a55-4cb2-a31e-3fe3f598c469&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-09-12T00%3A38%3A54Z&ske=2025-09-13T00%3A38%3A54Z&sks=b&skv=2024-08-04&sig=MBoVJ92ezHVtUmrZ0gMHh6vCnytYXBCwLR9t4O%2BSLgU%3D" alt="Dynamic Image">
        
        <!-- The overlaying caption -->
        <div class="image-caption">
            <div id="caption-title" class="caption-title">cat</div>
            <div id="caption-text" class="caption-text">cat with a goddamned hat</div>
        </div>
    </div>

</body>
</html>
