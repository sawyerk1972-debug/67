<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DoomScroll - Endless Short Videos</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: #000;
            color: #fff;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            overflow: hidden;
        }

        /* Main feed layout */
        .app-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            width: 100vw;
        }

        .video-container {
            width: 100%;
            max-width: 450px;
            height: 100vh;
            max-height: 900px;
            background-color: #111;
            position: relative;
            overflow-y: scroll;
            scroll-snap-type: y mandatory;
            scrollbar-width: none; /* Hide scrollbar for Firefox */
        }

        .video-container::-webkit-scrollbar {
            display: none; /* Hide scrollbar for Chrome/Safari */
        }

        /* Individual video card */
        .video-card {
            width: 100%;
            height: 100%;
            scroll-snap-align: start;
            scroll-snap-stop: always;
            position: relative;
            background-color: #000;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Overlay UI elements */
        .sidebar {
            position: absolute;
            right: 15px;
            bottom: 100px;
            display: flex;
            flex-direction: column;
            gap: 20px;
            align-items: center;
            z-index: 10;
        }

        .action-btn {
            background: rgba(0, 0, 0, 0.5);
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            color: white;
            font-size: 24px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.1s;
        }

        .action-btn:active {
            transform: scale(0.9);
        }

        .btn-label {
            font-size: 12px;
            margin-top: 4px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.8);
        }

        .action-group {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .video-info {
            position: absolute;
            left: 15px;
            bottom: 30px;
            right: 80px;
            z-index: 10;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.8);
        }

        .video-info h3 {
            font-size: 16px;
            margin-bottom: 8px;
        }

        .video-info p {
            font-size: 14px;
            color: #ddd;
        }

        /* Top Bar & Floating Post Button */
        .header {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            z-index: 20;
            background: linear-gradient(to bottom, rgba(0,0,0,0.7), transparent);
            max-width: 450px;
            left: 50%;
            transform: translateX(-50%);
        }

        .logo {
            font-weight: bold;
            font-size: 20px;
            letter-spacing: 1px;
            background: linear-gradient(45deg, #ff0055, #00f2fe);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .post-trigger-btn {
            background: #ff0055;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 20px;
            font-weight: bold;
            cursor: pointer;
        }

        /* Upload Modal Popup */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.85);
            z-index: 100;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .modal-content {
            background: #222;
            padding: 25px;
            border-radius: 16px;
            width: 100%;
            max-width: 400px;
            border: 1px solid #333;
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }

        .close-btn {
            background: none;
            border: none;
            color: #aaa;
            font-size: 24px;
            cursor: pointer;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-size: 14px;
            color: #aaa;
        }

        .form-group input[type="text"], 
        .form-group input[type="file"] {
            width: 100%;
            padding: 10px;
            background: #111;
            border: 1px solid #444;
            color: white;
            border-radius: 8px;
        }

        .submit-btn {
            width: 100%;
            padding: 12px;
            background: #00f2fe;
            color: black;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            margin-top: 10px;
        }

        .error-msg {
            color: #ff0055;
            font-size: 13px;
            margin-top: 5px;
            display: none;
        }
    </style>
</head>
<body>

    <div class="app-container">
        <!-- Floating Header -->
        <div class="header">
            <div class="logo">DOOMSCROLL</div>
            <button class="post-trigger-btn" onclick="openModal()">+ Post</button>
        </div>

        <!-- Video Scroll Feed -->
        <div class="video-container" id="feed">
            <!-- Videos will be dynamically populated here -->
        </div>
    </div>

    <!-- Upload Modal -->
    <div class="modal" id="uploadModal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Upload Short</h2>
                <button class="close-btn" onclick="closeModal()">&times;</button>
            </div>
            <div class="form-group">
                <label for="username">Username</label>
                <input type="text" id="username" placeholder="@yourname" value="@creator">
            </div>
            <div class="form-group">
                <label for="caption">Caption</label>
                <input type="text" id="caption" placeholder="Add a description...">
            </div>
            <div class="form-group">
                <label for="videoFile">Select Video (Max 20 seconds)</label>
                <input type="file" id="videoFile" accept="video/*">
                <div class="error-msg" id="validationError">Video must be 20 seconds or less.</div>
            </div>
            <button class="submit-btn" onclick="handleUpload()">Publish</button>
        </div>
    </div>

    <script>
        // Seed database mimicking global multi-user access via LocalStorage 
        // In a real app, this array would fetch from a cloud database (Node.js/Firebase/Supabase)
        const DEFAULT_VIDEOS = [
            {
                id: 1,
                url: "https://mixkit.co",
                username: "@nature_seeker",
                caption: "Staring into the sky 🌟 #aesthetic #calm",
                likes: 1204
            },
            {
                id: 2,
                url: "https://mixkit.co",
                username: "@ocean_vibes",
                caption: "Unwind your mind with these waves 🌊 #relaxing #satisfying",
                likes: 4590
            }
        ];

        let database = JSON.parse(localStorage.getItem('doomscroll_videos')) || DEFAULT_VIDEOS;
        const feed = document.getElementById('feed');

        // Render the feed
        function renderFeed() {
            feed.innerHTML = '';
            
            // To create an infinite "doomscroll" experience, we loop the content array a few times 
            // Mocking an endless supply of user generated content
            const infiniteLoopList = [...database, ...database, ...database];

            infiniteLoopList.forEach((item, index) => {
                const card = document.createElement('div');
                card.className = 'video-card';
                
                card.innerHTML = `
                    <video src="${item.url}" loop muted playsinline data-index="${index}"></video>
                    <div class="sidebar">
                        <div class="action-group">
                            <button class="action-btn" onclick="toggleLike(this)">❤️</button>
                            <span class="btn-label">${item.likes}</span>
                        </div>
                        <div class="action-group">
                            <button class="action-btn">💬</button>
                            <span class="btn-label">Reply</span>
                        </div>
                        <div class="action-group">
                            <button class="action-btn">🔗</button>
                            <span class="btn-label">Share</span>
