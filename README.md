<!DOCTYPE html>
<html lang="en">
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Content Creator Transformation Matrix</title>
    <style>
        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --primary: #38bdf8;
            --primary-glow: rgba(56, 189, 248, 0.15);
            --accent: #f43f5e;
            --success: #10b981;
            --warning: #f59e0b;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            padding: 2rem;
            line-height: 1.5;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            margin-bottom: 2.5rem;
            text-align: center;
        }

        header h1 {
            font-size: 2.5rem;
            font-weight: 800;
            margin-bottom: 0.5rem;
            background: linear-gradient(to right, var(--primary), #a855f7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        header p {
            color: var(--text-muted);
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto;
        }

        .dashboard-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 2rem;
        }

        @media (min-width: 1024px) {
            .dashboard-grid {
                grid-template-columns: 380px 1fr;
            }
        }

        /* Controls Section */
        .controls-card {
            background: var(--card-bg);
            border-radius: 16px;
            padding: 2rem;
            border: 1px solid #334155;
            height: fit-content;
            position: sticky;
            top: 2rem;
        }

        .controls-card h2 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
            border-bottom: 1px solid #334155;
            padding-bottom: 0.5rem;
        }

        .slider-group {
            margin-bottom: 1.8rem;
        }

        .slider-label-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 0.5rem;
        }

        .slider-title {
            font-weight: 600;
            font-size: 0.95rem;
        }

        .slider-value {
            font-size: 0.85rem;
            font-weight: bold;
            background: #0f172a;
            padding: 0.2rem 0.6rem;
            border-radius: 20px;
            border: 1px solid #475569;
        }

        .slider-desc {
            font-size: 0.8rem;
            color: var(--text-muted);
            margin-bottom: 0.5rem;
        }

        input[type="range"] {
            -webkit-appearance: none;
            width: 100%;
            height: 6px;
            border-radius: 3px;
            background: #475569;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: var(--primary);
            cursor: pointer;
            transition: transform 0.1s ease;
            box-shadow: 0 0 10px rgba(56, 189, 248, 0.5);
        }

        input[type="range"]::-webkit-slider-thumb:hover {
            transform: scale(1.2);
        }

        /* Impact Section */
        .impact-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .impact-card {
            background: var(--card-bg);
            border-radius: 14px;
            padding: 1.5rem;
            border: 1px solid #334155;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .impact-card.highlight {
            border-color: var(--primary);
            box-shadow: 0 4px 20px var(--primary-glow);
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }

        .card-title {
            font-size: 1.1rem;
            font-weight: 700;
        }

        .metric-badge {
            font-size: 1.25rem;
            font-weight: 800;
            color: var(--primary);
        }

        /* Progress Bar */
        .progress-container {
            background: #0f172a;
            border-radius: 8px;
            height: 8px;
            width: 100%;
            margin-bottom: 1rem;
            overflow: hidden;
            border: 1px solid #334155;
        }

        .progress-bar {
            height: 100%;
            width: 50%;
            background: linear-gradient(to right, #38bdf8, #a855f7);
            border-radius: 8px;
            transition: width 0.4s cubic-bezier(0.1, 0.8, 0.2, 1);
        }

        .dynamic-text {
            font-size: 0.9rem;
            color: var(--text-muted);
            min-height: 4.5rem;
        }

        .tag {
            display: inline-block;
            font-size: 0.75rem;
            padding: 0.15rem 0.5rem;
            border-radius: 4px;
            margin-top: 0.5rem;
            font-weight: 600;
        }
        .tag-positive { background: rgba(16, 185, 129, 0.15); color: #34d399; }
        .tag-negative { background: rgba(244, 63, 94, 0.15); color: #fb7185; }
        .tag-neutral { background: rgba(148, 163, 184, 0.15); color: #cbd5e1; }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>AI Creator Transformation Matrix</h1>
        <p>Adjust the systemic drivers below to explore how AI variables interact dynamically to remodel the production, quality, and economics of modern digital video creation.</p>
    </header>

    <div class="dashboard-grid">
        <!-- Input Sliders Area -->
        <div class="controls-card">
            <h2>Systemic Drivers</h2>
            
            <!-- Adoption -->
            <div class="slider-group">
                <div class="slider-label-container">
                    <span class="slider-title" style="color: #60a5fa;">🚀 Tool Adoption</span>
                    <span class="slider-value" id="val-adoption">50%</span>
                </div>
                <div class="slider-desc">Market saturation rate of automated scripts, editing workflows, and digital twins among creators.</div>
                <input type="range" id="slide-adoption" min="0" max="100" value="50">
            </div>

            <!-- Training -->
            <div class="slider-group">
                <div class="slider-label-container">
                    <span class="slider-title" style="color: #34d399;">🧠 Creator Literacy</span>
                    <span class="slider-value" id="val-training">50%</span>
                </div>
                <div class="slider-desc">Depth of user training regarding prompting precision, editing hybridity, and output engineering.</div>
                <input type="range" id="slide-training" min="0" max="100" value="50">
            </div>

            <!-- Access -->
            <div class="slider-group">
                <div class="slider-label-container">
                    <span class="slider-title" style="color: #a78bfa;">🔓 Technology Access</span>
                    <span class="slider-value" id="val-access">50%</span>
                </div>
                <div class="slider-desc">Democratization index: affordability of multimodal compute tiers vs. closed proprietary hardware walls.</div>
                <input type="range" id="slide-access" min="0" max="100" value="50">
            </div>

            <!-- Policies -->
            <div class="slider-group">
                <div class="slider-label-container">
                    <span class="slider-title" style="color: #fb7185;">⚖️ Platform Regulation</span>
                    <span class="slider-value" id="val-policies">50%</span>
                </div>
                <div class="slider-desc">Stringency of algorithmic penalization, synthetic labeling enforcement, and copyright protection bounds.</div>
                <input type="range" id="slide-policies" min="0" max="100" value="50">
            </div>
        </div>

        <!-- Output Impact Cards -->
        <div class="impact-container">
            
            <!-- Efficiency -->
            <div class="impact-card" id="card-efficiency">
                <div>
                    <div class="card-header">
                        <span class="card-title">⚡ Production Efficiency</span>
                        <span class="metric-badge" id="num-efficiency">50%</span>
                    </div>
                    <div class="progress-container">
                        <div class="progress-bar" id="bar-efficiency"></div>
                    </div>
                </div>
                <div>
                    <p class="dynamic-text" id="text-efficiency">Loading insight...</p>
                    <span class="tag" id="tag-efficiency">Neutral</span>
                </div>
            </div>

            <!-- Human Creativity -->
            <div class="impact-card" id="card-creativity">
                <div>
                    <div class="card-header">
                        <span class="card-title">🎨 Human Creativity Range</span>
                        <span class="metric-badge" id="num-creativity">50%</span>
                    </div>
