<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- 
      SEO & METADATA
      Instructions: Fill in the content attributes below to improve your site's SEO.
    -->
    <title>AI Hub - Your Multi AI Tools Hub</title>
    <meta name="description" content="AI Hub is an all-in-one platform for AI tools, including a prompt generator, image generator, background remover, text-to-speech, and article summarizer.">
    <meta name="keywords" content="AI, Artificial Intelligence, Midjourney, ChatGPT, Stable Diffusion, Image Generator, Background Remover, Text-to-Speech, Summarizer">
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://your-website.com/">
    <meta property="og:title" content="AI Hub - Your Multi AI Tools Hub">
    <meta property="og:description" content="All-in-one platform for AI tools: Prompting, Image Generation, BG Removal, and more.">
    <!-- Instruction: Replace with a URL to your site's logo or a featured image. -->
    <meta property="og:image" content="https://your-website.com/og-image.png">

    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://your-website.com/">
    <meta property="twitter:title" content="AI Hub - Your Multi AI Tools Hub">
    <meta property="twitter:description" content="All-in-one platform for AI tools: Prompting, Image Generation, BG Removal, and more.">
    <!-- Instruction: Replace with a URL to your site's logo or a featured image. -->
    <meta property="twitter:image" content="https://your-website.com/og-image.png">

    <!-- 
      GOOGLE ANALYTICS
      Instruction: Replace {{GA_MEASUREMENT_ID}} with your Google Analytics 4 Measurement ID.
    -->
    <script async src="https://www.googletagmanager.com/gtag/js?id={{GA_MEASUREMENT_ID}}"></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());
      // gtag('config', '{{GA_MEASUREMENT_ID}}'); // Uncomment this line and replace the ID.
    </script>
    
    <style>
        /* CSS RESET & FONT */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
        
        :root {
            --bg-color: #1f2937; /* Dark Slate Blue */
            --surface-color: #1f2937;
            --primary-color: #6366F1; /* Indigo */
            --primary-hover-color: #4F46E5;
            --text-color: #e5e7eb;
            --text-muted-color: #9ca3af;
            --border-color: rgba(255, 255, 255, 0.05);
            --success-color: #10b981;
            --error-color: #ef4444;

            --font-family: 'Inter', sans-serif;
            --border-radius: 12px;
            
            /* 3D / Neumorphic Shadows */
            --shadow-outset: 4px 4px 8px #111827, -4px -4px 8px #2d3a47;
            --shadow-inset: inset 4px 4px 8px #111827, inset -4px -4px 8px #2d3a47;
            --shadow-inset-light: inset 2px 2px 4px #111827, inset -2px -2px 4px #2d3a47;
        }

        body[data-theme="light"] {
            --bg-color: #f3f4f6; /* Gray 100 */
            --surface-color: #ffffff;
            --text-color: #111827; /* Gray 900 */
            --text-muted-color: #6b7280; /* Gray 500 */
            --border-color: #e5e7eb; /* Gray 200 */
            
            --shadow-outset: 5px 5px 10px #d1d9e6, -5px -5px 10px #ffffff;
            --shadow-inset: inset 5px 5px 10px #d1d9e6, inset -5px -5px 10px #ffffff;
            --shadow-inset-light: inset 2px 2px 5px #d1d9e6, inset -2px -2px 5px #ffffff;
        }

        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-family);
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            font-size: 16px;
            transition: background-color 0.3s, color 0.3s;
        }

        /* LAYOUT & STRUCTURE */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            padding: 1rem 0;
            position: sticky;
            top: 0;
            background-color: rgba(31, 41, 55, 0.8);
            backdrop-filter: blur(10px);
            z-index: 100;
            border-bottom: 1px solid var(--border-color);
        }

        body[data-theme="light"] header {
            background-color: rgba(255, 255, 255, 0.8);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.75rem;
            font-weight: 700;
            color: var(--text-color);
            text-decoration: none;
        }
        .logo span {
            color: var(--primary-color);
        }

        .user-info {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        #theme-toggle-btn {
            width: 44px;
            height: 44px;
            padding: 0;
            border-radius: 50%;
        }

        .credits {
            background-color: var(--bg-color);
            padding: 0.5rem 1rem;
            border-radius: var(--border-radius);
            font-weight: 600;
            box-shadow: var(--shadow-inset-light);
        }
        .credits span { color: var(--primary-color); font-weight: 700; }

        main {
            padding: 2rem 0;
        }

        footer {
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
            border-top: 1px solid var(--border-color);
            color: var(--text-muted-color);
        }
        
        /* TABS / TOOL SWITCHER */
        .tools-hub {
            background-color: var(--surface-color);
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-outset);
            overflow: hidden;
        }

        .tabs {
            display: flex;
            background-color: var(--bg-color);
            padding: 0.5rem;
            gap: 0.5rem;
            border-bottom: 1px solid var(--border-color);
            overflow-x: auto;
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
        .tabs::-webkit-scrollbar { display: none; }

        .tab-link {
            padding: 0.75rem 1.25rem;
            cursor: pointer;
            border: none;
            background-color: transparent;
            color: var(--text-muted-color);
            font-size: 0.95rem;
            font-weight: 600;
            border-radius: var(--border-radius);
            transition: all 0.2s ease-in-out;
            white-space: nowrap;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        .tab-link svg {
            width: 20px;
            height: 20px;
        }
        .tab-link:hover {
            background-color: rgba(255, 255, 255, 0.05);
            color: var(--text-color);
        }
        body[data-theme="light"] .tab-link:hover {
            background-color: rgba(0, 0, 0, 0.05);
        }
        .tab-link.active {
            color: var(--text-color);
            background-color: var(--primary-color);
            box-shadow: 0 2px 10px rgba(99, 102, 241, 0.3);
        }

        .tool-panel {
            display: none;
            padding: 2rem;
            animation: fadeIn 0.5s;
        }
        .tool-panel.active { display: block; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* UI COMPONENTS */
        .tool-card {
            background-color: var(--surface-color);
            padding: 1.5rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-outset);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--text-muted-color);
        }

        .input, select, textarea {
            width: 100%;
            padding: 0.85rem 1rem;
            background-color: var(--surface-color);
            border: none;
            border-radius: var(--border-radius);
            color: var(--text-color);
            font-size: 1rem;
            font-family: var(--font-family);
            transition: box-shadow 0.2s;
            box-shadow: var(--shadow-inset-light);
        }
        
        .input:focus, select:focus, textarea:focus {
            outline: none;
            box-shadow: var(--shadow-inset-light), 0 0 0 3px rgba(99, 102, 241, 0.4);
        }

        textarea {
            min-height: 120px;
            resize: vertical;
        }

        .btn {
            padding: 0.85rem 1.5rem;
            font-size: 1rem;
            font-weight: 600;
            border: none;
            border-radius: var(--border-radius);
            cursor: pointer;
            transition: all 0.2s ease-in-out;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            box-shadow: var(--shadow-outset);
        }

        .btn:active {
            box-shadow: var(--shadow-inset);
            transform: translateY(1px);
        }

        .btn-primary {
            background-color: var(--primary-color);
            color: white;
        }
        .btn-primary:hover {
            background-color: var(--primary-hover-color);
        }
        
        .btn-secondary {
            background-color: var(--surface-color);
            color: var(--text-color);
        }
        .btn-secondary:hover {
            background-color: #374151; /* Gray-600 */
        }
        body[data-theme="light"] .btn-secondary:hover {
            background-color: #f3f4f6; /* Gray-100 */
        }

        .btn:disabled {
            background-color: #374151;
            color: var(--text-muted-color);
            cursor: not-allowed;
            box-shadow: var(--shadow-inset-light);
        }
        body[data-theme="light"] .btn:disabled {
            background-color: #e5e7eb;
            color: #9ca3af;
        }

        .output-area {
            margin-top: 1.5rem;
            padding: 1.5rem;
            background-color: var(--bg-color);
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-inset);
            min-height: 100px;
            white-space: pre-wrap;
            word-wrap: break-word;
            position: relative;
        }
        
        .output-area .copy-btn {
            position: absolute;
            top: 0.75rem;
            right: 0.75rem;
        }

        .spinner {
            width: 20px;
            height: 20px;
            border: 2px solid rgba(255,255,255,0.3);
            border-top-color: var(--text-color);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        body[data-theme="light"] .spinner {
            border: 2px solid rgba(0,0,0,0.1);
            border-top-color: var(--text-color);
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* MODAL STYLES */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(17, 24, 39, 0.8);
            backdrop-filter: blur(5px);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s, visibility 0.3s;
        }
        
        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal {
            background-color: var(--surface-color);
            padding: 2rem;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-outset);
            width: 90%;
            max-width: 500px;
            transform: scale(0.95);
            transition: transform 0.3s;
        }
        
        .modal-overlay.active .modal {
            transform: scale(1);
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .modal-header h2 {
            margin: 0;
        }

        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text-muted-color);
            cursor: pointer;
            transition: color 0.2s;
        }
        .close-modal:hover { color: var(--text-color); }

        /* TOOL-SPECIFIC STYLES */
        #image-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }
        #image-gallery img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-outset);
        }

        #bgone-dropzone {
            border-radius: var(--border-radius);
            padding: 2rem;
            text-align: center;
            cursor: pointer;
            transition: box-shadow 0.2s;
            box-shadow: var(--shadow-inset);
        }
        #bgone-dropzone.dragover {
            box-shadow: var(--shadow-inset), 0 0 0 3px rgba(99, 102, 241, 0.4);
        }
        #bgone-previews {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
            justify-content: center;
        }
        #bgone-previews > div {
            flex-basis: 50%;
            text-align: center;
        }
        #bgone-previews img {
            width: 100%;
            height: auto;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-outset);
        }
        
        /* RESPONSIVENESS */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }
            .tool-panel {
                padding: 1.5rem 1rem;
            }
            .tabs {
                padding: 0.5rem;
            }
            .tab-link {
                padding: 0.75rem 1rem;
            }
            .tab-link span {
                display: none; /* Hide text on small screens */
            }
        }
    </style>
<script type="importmap">
{
  "imports": {
    "@google/genai": "https://esm.sh/@google/genai@^1.13.0"
  }
}
</script>
</head>
<body>

    <header>
        <div class="container header-content">
            <a href="#" class="logo">AI<span>Hub</span></a>
            <div class="user-info">
                <button id="theme-toggle-btn" class="btn btn-secondary" title="Toggle theme" aria-label="Toggle color theme">
                    <svg id="theme-icon-sun" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="5"/><path d="M12 1v2"/><path d="M12 21v2"/><path d="m4.22 4.22 1.42 1.42"/><path d="m18.36 18.36 1.42 1.42"/><path d="M1 12h2"/><path d="M21 12h2"/><path d="m4.22 19.78 1.42-1.42"/><path d="m18.36 5.64 1.42-1.42"/></svg>
                    <svg id="theme-icon-moon" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="display: none;"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg>
                </button>
                <div class="credits">Credits: <span id="credits-display">0</span></div>
                <button class="btn btn-secondary" id="buy-credits-btn">Buy Credits</button>
            </div>
        </div>
    </header>

    <main class="container">
        <div class="tools-hub">
            <nav class="tabs">
                <button class="tab-link active" data-tab="prompt-generator" title="Prompt Generator">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 3a6.364 6.364 0 0 0-6.364 6.364l-1.518 1.518A1.5 1.5 0 0 0 5.636 13h12.728a1.5 1.5 0 0 0 1.518-2.118l-1.518-1.518A6.364 6.364 0 0 0 12 3z"/><path d="M12 13v8"/><path d="M8 21h8"/></svg>
                    <span>Prompt Generator</span>
                </button>
                <button class="tab-link" data-tab="image-generator" title="Image Generator">
                     <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="18" height="18" x="3" y="3" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><path d="m21 15-5-5L5 21"/></svg>
                    <span>Image Generator</span>
                </button>
                <button class="tab-link" data-tab="bg-remover" title="Background Remover">
                     <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m12 3-1.912 5.813a2 2 0 0 1-1.275 1.275L3 12l5.813 1.912a2 2 0 0 1 1.275 1.275L12 21l1.912-5.813a2 2 0 0 1 1.275-1.275L21 12l-5.813-1.912a2 2 0 0 1-1.275-1.275L12 3Z"/><path d="M5 3v4"/><path d="M19 17v4"/><path d="M3 5h4"/><path d="M17 19h4"/></svg>
                    <span>BG Remover</span>
                </button>
                <button class="tab-link" data-tab="tts-stt" title="Text-to-Speech / Speech-to-Text">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2a3 3 0 0 0-3 3v7a3 3 0 0 0 6 0V5a3 3 0 0 0-3-3Z"/><path d="M19 10v2a7 7 0 0 1-14 0v-2"/><line x1="12" x2="12" y1="19" y2="22"/></svg>
                    <span>TTS/STT</span>
                </button>
                <button class="tab-link" data-tab="summarizer" title="Summarizer">
                     <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 22h16a2 2 0 0 0 2-2V4a2 2 0 0 0-2-2H8a2 2 0 0 0-2 2v16a2 2 0 0 1-2 2Zm0 0a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h4"/><path d="M14 10h2"/><path d="M14 14h4"/><path d="M14 6h4"/><path d="M9 6H7"/><path d="M9 10H7"/><path d="M9 14H7"/></svg>
                    <span>Summarizer</span>
                </button>
            </nav>
            <div class="tool-panels">
                <!-- Prompt Generator Panel -->
                <div id="prompt-generator" class="tool-panel active">
                    <h2>Prompt Generator</h2>
                    <p class="text-muted-color">Craft the perfect prompt for various AI models.</p>
                    <div class="form-group" style="margin-top: 2rem;">
                        <label for="prompt-desc">Describe what you want to generate</label>
                        <textarea id="prompt-desc" class="input" placeholder="e.g., A futuristic city skyline at sunset, with flying cars and neon lights"></textarea>
                    </div>
                    <div class="form-group">
                        <label for="prompt-model">Select Model Type</label>
                        <select id="prompt-model" class="input">
                            <option value="chatgpt">ChatGPT / Text</option>
                            <option value="midjourney">Midjourney</option>
                            <option value="stable-diffusion">Stable Diffusion</option>
                        </select>
                    </div>
                    <button id="generate-prompt-btn" class="btn btn-primary">Generate Prompt</button>
                    
                    <div id="prompt-output-area" class="output-area" style="display:none;">
                        <button class="btn btn-secondary copy-btn" data-target="#prompt-output">Copy</button>
                        <pre id="prompt-output"></pre>
                    </div>
                </div>

                <!-- Image Generator Panel -->
                <div id="image-generator" class="tool-panel">
                    <h2>Image Generator <span class="text-muted-color" id="image-cost"></span></h2>
                    <div class="form-group" style="margin-top: 2rem;">
                        <label for="image-prompt">Prompt</label>
                        <input type="text" id="image-prompt" class="input" placeholder="A cute red panda wearing a tiny chef hat">
                    </div>
                    <div class="form-group">
                        <label for="image-style">Style</label>
                        <select id="image-style" class="input">
                            <option value="realistic">Realistic</option>
                            <option value="anime">Anime</option>
                            <option value="3d-render">3D Render</option>
                            <option value="cartoon">Cartoon</option>
                        </select>
                    </div>
                    <button id="generate-image-btn" class="btn btn-primary">
                        <span class="btn-text">Generate Image</span>
                        <div class="spinner" style="display: none;"></div>
                    </button>
                    <div id="image-gallery" class="output-area">
                        <p class="text-muted-color">Your generated images will appear here.</p>
                    </div>
                </div>

                <!-- Background Remover Panel -->
                <div id="bg-remover" class="tool-panel">
                    <h2>Background Remover <span class="text-muted-color" id="bgone-cost"></span></h2>
                    <div id="bgone-dropzone" style="margin-top: 2rem;">
                        <p class="text-muted-color">Drag & drop an image here, or click to select a file.</p>
                        <input type="file" id="bgone-file-input" hidden accept="image/*">
                    </div>
                    <div id="bgone-previews" style="display:none;">
                        <div>
                            <p class="text-muted-color">Original</p>
                            <img id="bgone-original-preview" src="" alt="Original Image">
                        </div>
                        <div>
                            <p class="text-muted-color">Result</p>
                             <img id="bgone-result-preview" src="" alt="Image with background removed">
                        </div>
                    </div>
                    <div style="margin-top: 1.5rem;">
                        <button id="bgone-remove-btn" class="btn btn-primary" disabled>
                            <span class="btn-text">Remove Background</span>
                            <div class="spinner" style="display: none;"></div>
                        </button>
                        <button id="bgone-download-btn" class="btn btn-secondary" style="display:none;">Download Result</button>
                    </div>
                </div>

                <!-- TTS/STT Panel -->
                <div id="tts-stt" class="tool-panel">
                    <div class="tool-card" style="margin-bottom: 2rem;">
                        <h3>Text-to-Speech <span class="text-muted-color" id="tts-cost"></span></h3>
                        <div class="form-group" style="margin-top: 1.5rem;">
                            <label for="tts-text">Text</label>
                            <textarea id="tts-text" class="input" placeholder="Enter text to convert to speech..."></textarea>
                        </div>
                        <div class="form-group">
                            <label for="tts-voice">Voice</label>
                            <select id="tts-voice" class="input">
                                <option value="alloy">Alloy (Male)</option>
                                <option value="echo">Echo (Male)</option>
                                <option value="fable">Fable (Male)</option>
                                <option value="onyx">Onyx (Male)</option>
                                <option value="nova">Nova (Female)</option>
                                <option value="shimmer">Shimmer (Female)</option>
                            </select>
                        </div>
                        <button id="tts-generate-btn" class="btn btn-primary">
                             <span class="btn-text">Generate Speech</span>
                             <div class="spinner" style="display: none;"></div>
                        </button>
                        <div id="tts-output" class="output-area" style="display:none;"></div>
                    </div>
                    <div class="tool-card">
                        <h3>Speech-to-Text <span class="text-muted-color" id="stt-cost"></span></h3>
                        <div class="form-group" style="margin-top: 1.5rem;">
                            <label for="stt-file">Upload an audio file</label>
                            <input type="file" id="stt-file" class="input" accept="audio/*">
                        </div>
                         <button id="stt-transcribe-btn" class="btn btn-primary">
                             <span class="btn-text">Transcribe</span>
                             <div class="spinner" style="display: none;"></div>
                        </button>
                        <div id="stt-output" class="output-area" style="display:none;"></div>
                    </div>
                </div>

                <!-- Summarizer Panel -->
                <div id="summarizer" class="tool-panel">
                    <h2>Article Summarizer <span class="text-muted-color" id="summary-cost"></span></h2>
                    <div class="form-group" style="margin-top: 2rem;">
                        <label for="summary-input">Paste article text or URL</label>
                        <textarea id="summary-input" class="input" placeholder="Paste your text or a URL here..."></textarea>
                    </div>
                    <button id="summarize-btn" class="btn btn-primary">
                        <span class="btn-text">Summarize</span>
                        <div class="spinner" style="display: none;"></div>
                    </button>
                    <div id="summary-output-area" class="output-area" style="display:none;">
                         <button class="btn btn-secondary copy-btn" data-target="#summary-output">Copy</button>
                        <div id="summary-output"></div>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2024 AI Hub. All Rights Reserved.</p>
        </div>
    </footer>
    
    <!-- Modals -->
    <div id="login-modal" class="modal-overlay">
        <div class="modal">
            <div class="modal-header">
                <h2>Welcome to AI Hub</h2>
            </div>
            <div class="modal-body">
                <p>Enter your email to start. You'll get free credits to try our tools!</p>
                <div class="form-group" style="margin-top: 1rem;">
                    <label for="email-input">Email Address</label>
                    <input type="email" id="email-input" class="input" placeholder="you@example.com">
                </div>
                <button id="login-btn" class="btn btn-primary" style="width: 100%;">Get Started</button>
            </div>
        </div>
    </div>
    
    <div id="pricing-modal" class="modal-overlay">
        <div class="modal">
            <div class="modal-header">
                <h2>Out of Credits?</h2>
                <button class="close-modal" data-target="#pricing-modal">&times;</button>
            </div>
            <div class="modal-body">
                <p>Purchase more credits to continue using our AI tools.</p>
                <div style="background-color: var(--bg-color); padding: 1.5rem; border-radius: var(--border-radius); text-align: center; margin: 1.5rem 0; box-shadow: var(--shadow-inset);">
                    <h3>100 Credits</h3>
                    <p style="font-size: 2rem; font-weight: bold; color: var(--primary-color);">$10</p>
                </div>
                <button id="checkout-btn" class="btn btn-primary" style="width: 100%;">
                    <span class="btn-text">Proceed to Checkout</span>
                    <div class="spinner" style="display: none;"></div>
                </button>
            </div>
        </div>
    </div>

    <script type="module">
    import { GoogleGenAI } from '@google/genai';

    document.addEventListener('DOMContentLoaded', () => {

        // =================================================================================
        // CONFIGURATION & PLACEHOLDERS
        // Instructions: Replace these placeholder values with your actual configuration.
        // =================================================================================
        const CONFIG = {
            // --- API Endpoints ---
            API_URLS: {
                // NOTE: The Image Generator and Summarizer use the client-side Gemini API.
                BGONE_API: '{{BGONE_API_URL}}',            // e.g., 'https://your-backend.com/api/remove-bg'
                TTS_API: '{{TTS_API_URL}}',                // e.g., 'https://your-backend.com/api/tts'
                STT_API: '{{STT_API_URL}}',                // e.g., 'https://your-backend.com/api/stt'
                STRIPE_CHECKOUT_API: '{{STRIPE_CHECKOUT_SESSION_API}}', // e.g., 'https://your-backend.com/api/create-checkout-session'
            },
            
            // --- Stripe ---
            STRIPE_PUBLISHABLE_KEY: '{{STRIPE_PUBLISHABLE_KEY}}', // Your Stripe publishable key (pk_test_...)

            // --- Credits System ---
            FREE_CREDITS: 10,
            CREDIT_COSTS: {
                IMAGE_GENERATION: 2,
                BG_REMOVAL: 1,
                TTS: 1, // Per 1000 characters
                STT: 1, // Per minute of audio
                SUMMARY: 1,
            }
        };

        // =================================================================================
        // GLOBAL STATE & DOM ELEMENTS
        // =================================================================================
        let userSession = {
            email: null,
            credits: 0,
        };
        
        let ai; // Gemini AI client

        const DOM = {
            // Modals
            loginModal: document.getElementById('login-modal'),
            pricingModal: document.getElementById('pricing-modal'),
            
            // Header
            creditsDisplay: document.getElementById('credits-display'),
            buyCreditsBtn: document.getElementById('buy-credits-btn'),
            
            // Theme
            themeToggle: {
                btn: document.getElementById('theme-toggle-btn'),
                sunIcon: document.getElementById('theme-icon-sun'),
                moonIcon: document.getElementById('theme-icon-moon'),
            },

            // Tabs
            tabs: document.querySelectorAll('.tab-link'),
            toolPanels: document.querySelectorAll('.tool-panel'),
            
            // Prompt Generator
            promptGen: {
                desc: document.getElementById('prompt-desc'),
                model: document.getElementById('prompt-model'),
                generateBtn: document.getElementById('generate-prompt-btn'),
                outputArea: document.getElementById('prompt-output-area'),
                output: document.getElementById('prompt-output'),
            },

            // Image Generator
            imageGen: {
                prompt: document.getElementById('image-prompt'),
                style: document.getElementById('image-style'),
                generateBtn: document.getElementById('generate-image-btn'),
                gallery: document.getElementById('image-gallery'),
                cost: document.getElementById('image-cost'),
            },
            
            // BG Remover
            bgRemover: {
                dropzone: document.getElementById('bgone-dropzone'),
                fileInput: document.getElementById('bgone-file-input'),
                originalPreview: document.getElementById('bgone-original-preview'),
                resultPreview: document.getElementById('bgone-result-preview'),
                previewsContainer: document.getElementById('bgone-previews'),
                removeBtn: document.getElementById('bgone-remove-btn'),
                downloadBtn: document.getElementById('bgone-download-btn'),
                cost: document.getElementById('bgone-cost'),
                currentFile: null,
                resultBlob: null
            },
            
            // TTS/STT
            tts: {
                text: document.getElementById('tts-text'),
                voice: document.getElementById('tts-voice'),
                generateBtn: document.getElementById('tts-generate-btn'),
                output: document.getElementById('tts-output'),
                cost: document.getElementById('tts-cost'),
            },
            stt: {
                fileInput: document.getElementById('stt-file'),
                transcribeBtn: document.getElementById('stt-transcribe-btn'),
                output: document.getElementById('stt-output'),
                cost: document.getElementById('stt-cost'),
            },

            // Summarizer
            summarizer: {
                input: document.getElementById('summary-input'),
                summarizeBtn: document.getElementById('summarize-btn'),
                outputArea: document.getElementById('summary-output-area'),
                output: document.getElementById('summary-output'),
                cost: document.getElementById('summary-cost'),
            },
        };

        // =================================================================================
        // INITIALIZATION
        // =================================================================================
        function init() {
            // The execution environment MUST provide process.env.API_KEY for the summarizer to work.
            try {
                 ai = new GoogleGenAI({ apiKey: process.env.API_KEY });
            } catch (e) {
                console.warn(`Gemini client failed to initialize. Client-side AI tools will use offline fallbacks. Ensure 'process.env.API_KEY' is available.`);
            }
            
            initTheme();
            initUserSession();
            initEventListeners();
            initTabs();
            updateCreditCostsUI();
        }

        function initUserSession() {
            const storedEmail = localStorage.getItem('aihub_email');
            const storedCredits = localStorage.getItem('aihub_credits');

            if (storedEmail) {
                userSession.email = storedEmail;
                userSession.credits = storedCredits ? parseInt(storedCredits, 10) : CONFIG.FREE_CREDITS;
                updateCreditsDisplay();
            } else {
                DOM.loginModal.classList.add('active');
            }
        }
        
        function updateCreditCostsUI() {
            DOM.imageGen.cost.textContent = `(${CONFIG.CREDIT_COSTS.IMAGE_GENERATION} credits)`;
            DOM.bgRemover.cost.textContent = `(${CONFIG.CREDIT_COSTS.BG_REMOVAL} credit)`;
            DOM.tts.cost.textContent = `(${CONFIG.CREDIT_COSTS.TTS} credit/1k chars)`;
            DOM.stt.cost.textContent = `(${CONFIG.CREDIT_COSTS.STT} credit/min)`;
            DOM.summarizer.cost.textContent = `(${CONFIG.CREDIT_COSTS.SUMMARY} credit)`;
        }

        // =================================================================================
        // EVENT LISTENERS
        // =================================================================================
        function initEventListeners() {
            // Theme
            DOM.themeToggle.btn.addEventListener('click', handleThemeToggle);

            // Modals
            document.getElementById('login-btn').addEventListener('click', handleLogin);
            DOM.buyCreditsBtn.addEventListener('click', () => DOM.pricingModal.classList.add('active'));
            document.querySelectorAll('.close-modal').forEach(btn => {
                btn.addEventListener('click', () => document.querySelector(btn.dataset.target).classList.remove('active'));
            });
            document.getElementById('checkout-btn').addEventListener('click', handleStripeCheckout);

            // Copy buttons
            document.querySelectorAll('.copy-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    const content = document.querySelector(btn.dataset.target).innerText;
                    copyToClipboard(content, btn);
                });
            });
            
            // Tool event listeners
            initPromptGenListeners();
            initImageGenListeners();
            initBgRemoverListeners();
            initTtsSttListeners();
            initSummarizerListeners();
        }

        function initTabs() {
            DOM.tabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    DOM.tabs.forEach(t => t.classList.remove('active'));
                    DOM.toolPanels.forEach(p => p.classList.remove('active'));
                    
                    tab.classList.add('active');
                    document.getElementById(tab.dataset.tab).classList.add('active');
                });
            });
        }
        
        // =================================================================================
        // THEME MANAGEMENT
        // =================================================================================
        function applyTheme(theme) {
            if (theme === 'light') {
                document.body.dataset.theme = 'light';
                DOM.themeToggle.sunIcon.style.display = 'none';
                DOM.themeToggle.moonIcon.style.display = 'block';
                localStorage.setItem('aihub_theme', 'light');
            } else {
                document.body.dataset.theme = 'dark';
                DOM.themeToggle.sunIcon.style.display = 'block';
                DOM.themeToggle.moonIcon.style.display = 'none';
                localStorage.setItem('aihub_theme', 'dark');
            }
        }

        function handleThemeToggle() {
            const currentTheme = document.body.dataset.theme || 'dark';
            const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
            applyTheme(newTheme);
        }

        function initTheme() {
            const savedTheme = localStorage.getItem('aihub_theme');
            const systemPrefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
            // Use saved theme, or fall back to system preference
            const initialTheme = savedTheme || (systemPrefersDark ? 'dark' : 'light');
            applyTheme(initialTheme);
        }
        
        // =================================================================================
        // USER & CREDITS MANAGEMENT
        // =================================================================================
        function handleLogin() {
            const emailInput = document.getElementById('email-input');
            const email = emailInput.value.trim();
            if (email && /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
                userSession.email = email;
                userSession.credits = CONFIG.FREE_CREDITS;
                localStorage.setItem('aihub_email', email);
                localStorage.setItem('aihub_credits', userSession.credits);
                updateCreditsDisplay();
                DOM.loginModal.classList.remove('active');
            } else {
                alert('Please enter a valid email address.');
            }
        }

        function updateCreditsDisplay() {
            DOM.creditsDisplay.textContent = userSession.credits;
        }

        function hasEnoughCredits(cost) {
            if (userSession.credits >= cost) {
                return true;
            } else {
                DOM.pricingModal.classList.add('active');
                return false;
            }
        }

        function deductCredits(cost) {
            userSession.credits -= cost;
            localStorage.setItem('aihub_credits', userSession.credits);
            updateCreditsDisplay();
        }

        // =================================================================================
        // STRIPE CHECKOUT
        // =================================================================================
        async function handleStripeCheckout() {
            if (!CONFIG.STRIPE_PUBLISHABLE_KEY.startsWith('pk_')) {
                alert('Stripe is not configured. Please add your publishable key in the script.');
                return;
            }

            toggleButtonSpinner(document.getElementById('checkout-btn'), true);
            
            // This is where you call your backend to create a Stripe Checkout Session.
            // Your backend should use your Stripe secret key to create the session
            // and return the session ID.
            try {
                const response = await fetch(CONFIG.API_URLS.STRIPE_CHECKOUT_API, {
                    method: 'POST',
                    headers: {'Content-Type': 'application/json'},
                    body: JSON.stringify({
                        email: userSession.email,
                        quantity: 1 // for 100 credits pack
                    })
                });

                if (!response.ok) throw new Error('Failed to create checkout session.');
                
                const { sessionId } = await response.json();

                const stripe = Stripe(CONFIG.STRIPE_PUBLISHABLE_KEY);
                const { error } = await stripe.redirectToCheckout({ sessionId });
                
                if (error) {
                    alert(error.message);
                }
            } catch (error) {
                console.error('Stripe checkout error:', error);
                alert('Could not initiate checkout. Please try again later.');
            } finally {
                toggleButtonSpinner(document.getElementById('checkout-btn'), false);
            }
        }
        
        // After a successful payment, Stripe will redirect to a success URL you configure.
        // On that page, you can confirm the payment and update the user's credits.
        // For MVPs, you can simply add credits on the success page load, e.g., by checking for a query param.
        // A robust solution uses Stripe Webhooks on your backend to securely confirm payments
        // and update the user's credit balance in a database.
        function addPurchasedCredits(amount) {
            userSession.credits += amount;
            localStorage.setItem('aihub_credits', userSession.credits);
            updateCreditsDisplay();
            DOM.pricingModal.classList.remove('active');
            alert(`Successfully added ${amount} credits!`);
        }

        // =================================================================================
        // TOOL: PROMPT GENERATOR
        // =================================================================================
        function initPromptGenListeners() {
            DOM.promptGen.generateBtn.addEventListener('click', generatePrompt);
        }

        function generatePrompt() {
            const desc = DOM.promptGen.desc.value;
            const model = DOM.promptGen.model.value;
            if (!desc) {
                alert("Please describe what you want to generate.");
                return;
            }

            let prompt = '';
            switch(model) {
                case 'midjourney':
                    prompt = `${desc} --ar 16:9 --v 6.0 --style raw`;
                    break;
                case 'stable-diffusion':
                    prompt = `(masterpiece, best quality), ${desc}, intricate details, cinematic lighting`;
                    break;
                case 'chatgpt':
                default:
                    prompt = `Generate a creative response for: "${desc}"`;
                    break;
            }

            DOM.promptGen.output.textContent = prompt;
            DOM.promptGen.outputArea.style.display = 'block';
        }
        
        // =================================================================================
        // TOOL: IMAGE GENERATOR
        // =================================================================================
        function initImageGenListeners() {
            DOM.imageGen.generateBtn.addEventListener('click', handleImageGeneration);
        }
        
        async function handleImageGeneration() {
            const cost = CONFIG.CREDIT_COSTS.IMAGE_GENERATION;
            if (!hasEnoughCredits(cost)) return;
            
            const prompt = DOM.imageGen.prompt.value;
            const style = DOM.imageGen.style.value;
            if (!prompt) {
                alert("Please enter a prompt.");
                return;
            }
            
            toggleButtonSpinner(DOM.imageGen.generateBtn, true);
            try {
                const imageUrl = await callImageAPI(prompt, style);
                
                // On success, deduct credits and show image
                deductCredits(cost);
                const img = document.createElement('img');
                img.src = imageUrl;
                img.alt = prompt;
                
                if (DOM.imageGen.gallery.querySelector('p')) {
                    DOM.imageGen.gallery.innerHTML = ''; // Clear initial message
                }
                DOM.imageGen.gallery.prepend(img);
                
            } catch (error) {
                console.error("Image generation failed:", error);
                alert(`Error: ${error.message}`);
            } finally {
                toggleButtonSpinner(DOM.imageGen.generateBtn, false);
            }
        }
        
        async function callImageAPI(prompt, style) {
            if (!ai) {
                throw new Error("Gemini client not initialized. Check API Key.");
            }

            let fullPrompt;
            const stylePrefixes = {
                'realistic': 'A realistic, high-definition photograph of:',
                'anime': 'An anime-style digital art of:',
                '3d-render': 'A cinematic 3D render of:, trending on ArtStation',
                'cartoon': 'A playful cartoon-style illustration of:',
            };
            
            fullPrompt = `${stylePrefixes[style] || ''} ${prompt}`;

            console.log(`Generating image with prompt: "${fullPrompt}"`);

            try {
                const response = await ai.models.generateImages({
                    model: 'imagen-3.0-generate-002',
                    prompt: fullPrompt,
                    config: {
                        numberOfImages: 1,
                        outputMimeType: 'image/jpeg',
                        aspectRatio: '1:1',
                    },
                });

                if (!response.generatedImages || response.generatedImages.length === 0) {
                    throw new Error('Image generation succeeded but returned no images.');
                }

                const base64ImageBytes = response.generatedImages[0].image.imageBytes;
                return `data:image/jpeg;base64,${base64ImageBytes}`;
            } catch(error) {
                console.error("Gemini Image generation API call failed:", error);
                throw new Error("The AI image generator failed. This could be due to a safety policy violation or an issue with the service. Please try a different prompt.");
            }
        }
        
        // =================================================================================
        // TOOL: BACKGROUND REMOVER
        // =================================================================================
        function initBgRemoverListeners() {
            const { dropzone, fileInput, removeBtn } = DOM.bgRemover;
            
            dropzone.addEventListener('click', () => fileInput.click());
            fileInput.addEventListener('change', (e) => handleFileSelect(e.target.files[0]));
            
            ['dragenter', 'dragover', 'dragleave', 'drop'].forEach(eventName => {
                dropzone.addEventListener(eventName, preventDefaults, false);
            });
            ['dragenter', 'dragover'].forEach(eventName => {
                dropzone.addEventListener(eventName, () => dropzone.classList.add('dragover'), false);
            });
            ['dragleave', 'drop'].forEach(eventName => {
                dropzone.addEventListener(eventName, () => dropzone.classList.remove('dragover'), false);
            });
            
            dropzone.addEventListener('drop', (e) => handleFileSelect(e.dataTransfer.files[0]));
            removeBtn.addEventListener('click', handleBgRemoval);
            DOM.bgRemover.downloadBtn.addEventListener('click', downloadBgRemovedImage);
        }
        
        function handleFileSelect(file) {
            if (!file || !file.type.startsWith('image/')) {
                alert('Please select an image file.');
                return;
            }
            
            DOM.bgRemover.currentFile = file;
            const reader = new FileReader();
            reader.onload = (e) => {
                DOM.bgRemover.originalPreview.src = e.target.result;
                DOM.bgRemover.previewsContainer.style.display = 'flex';
                DOM.bgRemover.resultPreview.src = ''; // Clear previous result
                DOM.bgRemover.downloadBtn.style.display = 'none';
                DOM.bgRemover.removeBtn.disabled = false;
            };
            reader.readAsDataURL(file);
        }
        
        async function handleBgRemoval() {
            const cost = CONFIG.CREDIT_COSTS.BG_REMOVAL;
            if (!hasEnoughCredits(cost)) return;
            if (!DOM.bgRemover.currentFile) return;
            
            toggleButtonSpinner(DOM.bgRemover.removeBtn, true);
            DOM.bgRemover.removeBtn.disabled = true;
            
            try {
                // Client-side image compression before upload
                const compressedFile = await compressImage(DOM.bgRemover.currentFile);
                
                // API call
                const resultBlob = await callBGoneAPI(compressedFile);
                DOM.bgRemover.resultBlob = resultBlob;
                
                const resultUrl = URL.createObjectURL(resultBlob);
                DOM.bgRemover.resultPreview.src = resultUrl;
                DOM.bgRemover.downloadBtn.style.display = 'inline-flex';
                
                deductCredits(cost);
            } catch (error) {
                console.error("Background removal failed:", error);
                alert(`Error: ${error.message}`);
            } finally {
                toggleButtonSpinner(DOM.bgRemover.removeBtn, false);
                // Re-enable button if there's a file
                if (DOM.bgRemover.currentFile) DOM.bgRemover.removeBtn.disabled = false;
            }
        }
        
        async function callBGoneAPI(file) {
            // This is a placeholder for your backend API call.
            console.log(`Calling BG Remover API for file: ${file.name}`);
            
            // --- SIMULATED API CALL ---
            await new Promise(resolve => setTimeout(resolve, 2000));
            throw new Error("Background Remover API not connected. See comments in HTML source.");
            // --- END SIMULATION ---
            
            /*
            // --- REAL API CALL (EXAMPLE) ---
            const formData = new FormData();
            formData.append('file', file);
            
            const response = await fetch(CONFIG.API_URLS.BGONE_API, {
                method: 'POST',
                // Your backend might need an API key header.
                // headers: { 'X-API-Key': 'YOUR_BGONE_API_KEY' },
                body: formData
            });
            
            if (!response.ok) {
                throw new Error('Background removal failed.');
            }
            
            return await response.blob(); // Expects the image file back
            */
        }
        
        function downloadBgRemovedImage() {
            if (!DOM.bgRemover.resultBlob) return;
            const url = URL.createObjectURL(DOM.bgRemover.resultBlob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'background-removed.png';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
        }

        // =================================================================================
        // TOOL: TTS / STT
        // =================================================================================
        function initTtsSttListeners() {
            DOM.tts.generateBtn.addEventListener('click', handleTtsGeneration);
            DOM.stt.transcribeBtn.addEventListener('click', handleSttTranscription);
        }

        async function handleTtsGeneration() {
            const text = DOM.tts.text.value;
            const cost = Math.ceil(text.length / 1000) * CONFIG.CREDIT_COSTS.TTS || CONFIG.CREDIT_COSTS.TTS;
            if (!hasEnoughCredits(cost)) return;
            
            if (!text) {
                alert('Please enter text for text-to-speech.');
                return;
            }

            toggleButtonSpinner(DOM.tts.generateBtn, true);
            try {
                const voice = DOM.tts.voice.value;
                const audioBlob = await callTTSAPI(text, voice);
                
                const audioUrl = URL.createObjectURL(audioBlob);
                const audio = new Audio(audioUrl);
                
                DOM.tts.output.innerHTML = '';
                DOM.tts.output.appendChild(audio);
                audio.controls = true;
                DOM.tts.output.style.display = 'block';

                deductCredits(cost);
            } catch (error) {
                console.error("TTS generation failed:", error);
                alert(`Error: ${error.message}`);
            } finally {
                toggleButtonSpinner(DOM.tts.generateBtn, false);
            }
        }
        
        async function callTTSAPI(text, voice) {
            console.log(`Calling TTS API for text: "${text.substring(0,30)}...", voice: "${voice}"`);
            await new Promise(resolve => setTimeout(resolve, 1500));
            throw new Error("TTS API not connected.");
        }
        
        async function handleSttTranscription() {
            const file = DOM.stt.fileInput.files[0];
            if (!file) {
                alert('Please select an audio file to transcribe.');
                return;
            }
            // Simple cost estimation, real implementation would get duration
            const cost = CONFIG.CREDIT_COSTS.STT;
            if (!hasEnoughCredits(cost)) return;

            toggleButtonSpinner(DOM.stt.transcribeBtn, true);
            try {
                const transcript = await callSTTAPI(file);
                DOM.stt.output.textContent = transcript;
                DOM.stt.output.style.display = 'block';
                deductCredits(cost);
            } catch (error) {
                console.error("STT transcription failed:", error);
                alert(`Error: ${error.message}`);
            } finally {
                toggleButtonSpinner(DOM.stt.transcribeBtn, false);
            }
        }
        
        async function callSTTAPI(audioFile) {
            console.log(`Calling STT API for file: ${audioFile.name}`);
            await new Promise(resolve => setTimeout(resolve, 2000));
            throw new Error("STT API not connected.");
        }
        
        // =================================================================================
        // TOOL: SUMMARIZER
        // =================================================================================
        function initSummarizerListeners() {
            DOM.summarizer.summarizeBtn.addEventListener('click', handleSummarization);
        }

        async function handleSummarization() {
            const cost = CONFIG.CREDIT_COSTS.SUMMARY;
            if (!hasEnoughCredits(cost)) return;
            
            const input = DOM.summarizer.input.value.trim();
            if (!input) {
                alert('Please paste text or a URL to summarize.');
                return;
            }

            toggleButtonSpinner(DOM.summarizer.summarizeBtn, true);
            try {
                const summary = await callSummaryAPI(input);
                DOM.summarizer.output.textContent = summary;
                DOM.summarizer.outputArea.style.display = 'block';
                deductCredits(cost);
            } catch (error) {
                console.error("Summarization failed:", error);
                alert(`${error.message}. Attempting client-side fallback.`);
                // Client-side fallback
                const fallbackSummary = clientSideSummarize(input);
                DOM.summarizer.output.textContent = "AI Summarizer is unavailable. Here is a basic summary:\n\n" + fallbackSummary;
                DOM.summarizer.outputArea.style.display = 'block';
            } finally {
                toggleButtonSpinner(DOM.summarizer.summarizeBtn, false);
            }
        }

        async function callSummaryAPI(text) {
            if (!ai) {
                throw new Error("Gemini client not initialized. Check API Key.");
            }
            
            console.log(`Calling Gemini API to summarize...`);
            try {
                const response = await ai.models.generateContent({
                    model: 'gemini-2.5-flash',
                    contents: `Summarize the following content in a concise paragraph: "${text}"`,
                    config: {
                        temperature: 0.3,
                        topK: 32,
                        topP: 1,
                    }
                });
                return response.text;
            } catch(error) {
                console.error("Gemini API call failed:", error);
                throw new Error("The AI summarizer failed. Please try again."); // Throw a new, more user-friendly error.
            }
        }

        function clientSideSummarize(text) {
            const sentences = text.match(/[^\.!\?]+[\.!\?]+/g) || [];
            if (sentences.length <= 3) {
                return text; // Return original if too short
            }
            // Return first and last sentence for a very basic summary
            return sentences[0].trim() + " (...) " + sentences[sentences.length - 1].trim();
        }

        // =================================================================================
        // HELPER UTILITIES
        // =================================================================================
        function toggleButtonSpinner(button, show) {
            const text = button.querySelector('.btn-text');
            const spinner = button.querySelector('.spinner');
            if (show) {
                if(text) text.style.display = 'none';
                if(spinner) spinner.style.display = 'inline-block';
                button.disabled = true;
            } else {
                if(text) text.style.display = 'inline-block';
                if(spinner) spinner.style.display = 'none';
                button.disabled = false;
            }
        }

        function copyToClipboard(text, button) {
            navigator.clipboard.writeText(text).then(() => {
                const originalText = button.textContent;
                button.textContent = 'Copied!';
                button.style.backgroundColor = 'var(--success-color)';
                setTimeout(() => {
                    button.textContent = originalText;
                    button.style.backgroundColor = '';
                }, 2000);
            }).catch(err => {
                console.error('Failed to copy text: ', err);
                alert('Failed to copy.');
            });
        }
        
        function preventDefaults(e) {
            e.preventDefault();
            e.stopPropagation();
        }

        function compressImage(file, maxWidth = 1600, maxHeight = 1600, quality = 0.8) {
            return new Promise((resolve, reject) => {
                const img = new Image();
                img.src = URL.createObjectURL(file);
                img.onload = () => {
                    const canvas = document.createElement('canvas');
                    let width = img.width;
                    let height = img.height;

                    if (width > height) {
                        if (width > maxWidth) {
                            height *= maxWidth / width;
                            width = maxWidth;
                        }
                    } else {
                        if (height > maxHeight) {
                            width *= maxHeight / height;
                            height = maxHeight;
                        }
                    }

                    canvas.width = width;
                    canvas.height = height;
                    const ctx = canvas.getContext('2d');
                    ctx.drawImage(img, 0, 0, width, height);

                    canvas.toBlob((blob) => {
                        resolve(new File([blob], file.name, {
                            type: 'image/jpeg',
                            lastModified: Date.now()
                        }));
                    }, 'image/jpeg', quality);
                };
                img.onerror = (error) => reject(error);
            });
        }
        
        // Load Stripe.js script dynamically
        const stripeScript = document.createElement('script');
        stripeScript.src = 'https://js.stripe.com/v3/';
        stripeScript.onload = () => {
            // Can initialize Stripe here if needed, but it's handled in the checkout function
        };
        document.head.appendChild(stripeScript);

        // Run app
        init();
    });
    </script>
    
<!--
==========================================================================================
// README: DEPLOYMENT & SETUP INSTRUCTIONS
==========================================================================================

Welcome to AI Hub! This is a front-end MVP. To make it fully functional, you need to set up a backend service to handle API keys and business logic securely.

**Step 1: Environment Setup for Gemini API**

The "Article Summarizer" and "Image Generator" tools use the Google Gemini API directly on the client-side.
For this to work, the API key must be available as `process.env.API_KEY` in the execution environment where this page is served. You CANNOT paste the key directly into this file.
- If using a build tool (like Vite, Webpack), you can use a `.env` file to set `API_KEY=YOUR_GEMINI_KEY`.
- If deploying on a platform like Vercel or Netlify, set `API_KEY` as an environment variable in the project settings.

**Step 2: Replace Placeholders in this file**

In the <script> section of this HTML file, find the `CONFIG` object and replace all `{{...}}` placeholders with your actual keys and URLs.

- `{{BGONE_API_URL}}`, `{{TTS_API_URL}}`, etc.: These are endpoints on your backend server. The Image Generator and Summarizer tools run directly in the browser and do not require separate backend endpoints.
- `{{STRIPE_PUBLISHABLE_KEY}}`: Your public key from the Stripe dashboard.
- `{{STRIPE_CHECKOUT_SESSION_API}}`: The endpoint on your backend that creates a Stripe Checkout session.
- `{{GA_MEASUREMENT_ID}}`: Your Google Analytics 4 ID.

**Step 3: Create a Backend Proxy Server**

Never expose your secret API keys (for services like Stripe, or paid background removal APIs) in client-side code.
Create a simple backend server (e.g., using Node.js/Express, Python/Flask, etc.) to act as a proxy for the remaining tools that require it (BG Remover, TTS, STT) and for handling Stripe payments.

**Example Node.js/Express proxy endpoint for a tool:**

```javascript
// server.js
const express = require('express');
const cors = require('cors');
const app = express();
app.use(cors()); // Enable CORS for your frontend
app.use(express.json());

// Your secret API key, stored as an environment variable for a service like BG Remover
const BGONE_API_KEY = process.env.BGONE_API_KEY; 

app.post('/api/remove-bg', async (req, res) => {
    // This is where you would handle file uploads and call the background removal service
    // For example, using 'formidable' for parsing multipart/form-data
    // and 'axios' or 'node-fetch' to call the third-party API.
    // ...
});

// Create similar endpoints for other tools (TTS, STT, Stripe)
// ...

const PORT = process.env.PORT || 3001;
app.listen(PORT, () => console.log(`Server running on port ${PORT}`));
```

**Step 4: Deploy your Backend**

Host your backend server on a platform like Render, Heroku, or a cloud provider (AWS, GCP, Azure).
- **Recommendation for beginners:** Render offers a simple free tier for web services.
- Ensure you use HTTPS for your live backend.
- Set your secret API keys as environment variables in your hosting provider's dashboard, NOT in your code.

**Step 5: Set up Stripe Checkout**

1. In your Stripe Dashboard, get your **Publishable Key** and **Secret Key**.
2. Create a backend endpoint (`/api/create-checkout-session`) that uses the Stripe Node.js library and your secret key to create a session.
3. Configure success and cancel URLs in the Stripe session creation call. The success URL should be a page on your site that can notify the user of the successful purchase and potentially trigger a credit update (though webhooks are more reliable).
4. **Implement Webhooks (Crucial for Production):**
   - Create a webhook endpoint on your backend (e.g., `/api/stripe-webhook`).
   - Listen for the `checkout.session.completed` event from Stripe.
   - When you receive this event, verify the signature to ensure it's from Stripe.
   - Securely update the user's credit balance in your database. This is the most reliable way to grant credits after a purchase.

By following these steps, you can turn this front-end template into a fully functional and secure web application.
-->
</body>
</html>
