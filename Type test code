<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ProType | Advanced Typing Platform</title>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    crossorigin="anonymous"
  />
  <style>
    /* styles.css content */
    :root {
        --primary: #4361ee;
        --primary-dark: #3a0ca3;
        --secondary: #4cc9f0;
        --accent: #f72585;
        --dark: #1e1e2e;
        --darker: #121212;
        --light: #f8f9fa;
        --gray: #6c757d;
        --success: #4caf50;
        --danger: #f44336;
        --warning: #ff9800;
        --shadow: 0 4px 20px rgba(0,0,0,0.2);
        --transition: all 0.3s ease-in-out;
    }

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
        background-color: var(--darker);
        color: var(--light);
        line-height: 1.6;
        transition: var(--transition);
        min-height: 100vh;
        overflow-x: hidden;
        display: flex;
        flex-direction: column;
    }

    .container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 20px;
        flex-grow: 1;
    }

    /* Header */
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px 0;
        position: sticky;
        top: 0;
        background: rgba(30, 30, 46, 0.95);
        z-index: 100;
        backdrop-filter: blur(10px);
        border-bottom: 1px solid rgba(255,255,255,0.1);
    }

    .logo {
        font-size: 2rem;
        font-weight: 700;
        background: linear-gradient(135deg, var(--primary), var(--secondary));
        -webkit-background-clip: text;
        background-clip: text;
        -webkit-text-fill-color: transparent;
        display: flex;
        align-items: center;
        gap: 10px;
        text-shadow: 0 0 5px rgba(255,255,255,0.3);
    }

    .logo i {
        font-size: 1.8rem;
        color: var(--primary);
    }

    nav ul {
        display: flex;
        list-style: none;
        gap: 30px;
    }

    nav a {
        color: var(--light);
        text-decoration: none;
        font-weight: 500;
        padding: 10px 15px;
        border-radius: 8px;
        transition: var(--transition);
        display: flex;
        align-items: center;
        gap: 8px;
        text-transform: uppercase;
        letter-spacing: 0.5px;
    }

    nav a:hover, nav a.active {
        background: rgba(67, 97, 238, 0.2);
        color: var(--secondary);
        transform: translateY(-2px);
        box-shadow: 0 5px 15px rgba(67, 97, 238, 0.2);
    }

    nav a i {
        font-size: 1.1rem;
    }

    /* Page Transitions */
    .page {
        display: none;
        animation: fadeIn 0.6s ease-out;
        padding: 20px 0;
    }

    .page.active {
        display: block;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(30px); }
        to { opacity: 1; transform: translateY(0); }
    }

    /* Welcome Page */
    .welcome-page {
        min-height: 80vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 40px 20px;
    }

    .welcome-content {
        max-width: 900px;
        width: 100%;
    }

    .welcome-banner {
        background: linear-gradient(135deg, var(--primary), var(--primary-dark));
        padding: 60px 40px;
        border-radius: 25px;
        margin: 30px 0;
        box-shadow: 0 15px 40px rgba(0,0,0,0.5);
        position: relative;
        overflow: hidden;
        border: 1px solid rgba(255,255,255,0.2);
    }

    .welcome-banner:before {
        content: "";
        position: absolute;
        top: -50%;
        left: -50%;
        width: 200%;
        height: 200%;
        background: radial-gradient(circle, rgba(255,255,255,0.15) 0%, transparent 70%);
        transform: rotate(30deg);
        animation: backgroundPulse 5s infinite alternate;
    }

    @keyframes backgroundPulse {
        from { opacity: 0.8; }
        to { opacity: 1; }
    }

    .welcome-banner h1 {
        font-size: 4rem;
        margin-bottom: 25px;
        position: relative;
        text-shadow: 0 0 10px rgba(0,0,0,0.5);
    }

    .welcome-banner p {
        font-size: 1.6rem;
        max-width: 750px;
        margin: 0 auto;
        position: relative;
        line-height: 1.5;
    }

    .features-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 30px;
        margin: 60px 0;
    }

    .feature-card {
        background: rgba(30, 30, 46, 0.8);
        border: 1px solid rgba(255,255,255,0.15);
        border-radius: 20px;
        padding: 35px;
        text-align: center;
        transition: var(--transition);
        backdrop-filter: blur(12px);
        box-shadow: var(--shadow);
        position: relative;
        overflow: hidden;
    }

    .feature-card:before {
        content: "";
        position: absolute;
        top: 0; left: 0;
        width: 100%; height: 100%;
        background: linear-gradient(135deg, rgba(67, 97, 238, 0.1) 0%, rgba(255,255,255,0) 50%);
        opacity: 0;
        transition: opacity 0.3s ease;
    }

    .feature-card:hover:before {
        opacity: 1;
    }

    .feature-card:hover {
        transform: translateY(-15px);
        border-color: var(--primary);
        box-shadow: 0 20px 40px rgba(67, 97, 238, 0.3);
    }

    .feature-icon {
        font-size: 3.5rem;
        margin-bottom: 25px;
        color: var(--secondary);
        text-shadow: 0 0 10px rgba(76, 201, 240, 0.5);
    }

    .feature-card h3 {
        font-size: 1.6rem;
        margin-bottom: 15px;
        color: var(--light);
    }

    .feature-card p {
        font-size: 1.1rem;
        color: var(--gray);
    }

    .cta-buttons {
        display: flex;
        gap: 25px;
        justify-content: center;
        margin-top: 50px;
        flex-wrap: wrap;
    }

    /* Buttons */
    .btn {
        padding: 15px 40px;
        border: none;
        border-radius: 50px;
        cursor: pointer;
        font-size: 1.1rem;
        font-weight: 600;
        transition: var(--transition);
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
        text-transform: uppercase;
        letter-spacing: 1px;
        box-shadow: var(--shadow);
        flex-shrink: 0;
    }

    .btn-primary {
        background: linear-gradient(135deg, var(--primary), var(--primary-dark));
        color: white;
    }

    .btn-secondary {
        background: transparent;
        color: var(--secondary);
        border: 2px solid var(--secondary);
    }

    .btn-accent {
        background: linear-gradient(135deg, var(--accent), #e71a7d);
        color: white;
    }

    .btn:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 25px rgba(0,0,0,0.4);
    }

    /* Typing Test Page */
    .test-container {
        background: rgba(30, 30, 46, 0.8);
        border-radius: 25px;
        padding: 35px;
        box-shadow: var(--shadow);
        backdrop-filter: blur(12px);
        border: 1px solid rgba(255,255,255,0.15);
        margin: 30px 0;
    }

    .test-header {
        display: flex;
        justify-content: space-between;
        margin-bottom: 30px;
        flex-wrap: wrap;
        gap: 20px;
    }

    .time-options {
        display: flex;
        gap: 15px;
        flex-wrap: wrap;
    }

    .time-btn {
        padding: 12px 25px;
        background: rgba(255,255,255,0.08);
        border: 1px solid rgba(255,255,255,0.15);
        border-radius: 50px;
        cursor: pointer;
        transition: var(--transition);
        color: var(--light);
        font-weight: 500;
        text-transform: uppercase;
    }

    .time-btn:hover, .time-btn.active {
        background: var(--primary);
        color: white;
        border-color: var(--primary);
        transform: translateY(-3px);
        box-shadow: 0 5px 15px rgba(67, 97, 238, 0.4);
    }

    .timer {
        font-size: 1.8rem;
        font-weight: 700;
        background: rgba(76, 201, 240, 0.15);
        padding: 12px 30px;
        border-radius: 50px;
        display: flex;
        align-items: center;
        gap: 10px;
        border: 1px solid rgba(76, 201, 240, 0.3);
    }

    .test-content {
        margin: 30px 0;
    }

    #typing-text {
        font-size: 1.7rem;
        line-height: 1.9;
        margin-bottom: 30px;
        min-height: 220px;
        padding: 30px;
        background: rgba(0,0,0,0.3);
        border-radius: 20px;
        border: 1px solid rgba(255,255,255,0.1);
        color: var(--light);
        position: relative;
        overflow: hidden;
        text-align: left;
    }

    .word {
        display: inline-block;
        margin: 0 8px 8px 0;
        padding: 6px 12px;
        border-radius: 10px;
        transition: var(--transition);
        white-space: pre-wrap;
    }

    .word.current {
        background: rgba(67, 97, 238, 0.4);
        color: white;
        box-shadow: 0 0 20px rgba(67, 97, 238, 0.6);
        transform: scale(1.02);
    }

    .char.correct {
        color: var(--success);
    }

    .char.incorrect {
        color: var(--danger);
        text-decoration: underline wavy var(--danger) 2px;
    }

    .cursor {
        display: inline-block;
        width: 3px;
        height: 1.4em;
        background: var(--secondary);
        vertical-align: middle;
        margin-left: 2px;
        animation: blink 0.8s infinite step-end;
        position: relative;
        z-index: 1;
    }

    @keyframes blink {
        0%, 100% { opacity: 1; }
        50% { opacity: 0; }
    }

    #typing-input {
        width: 100%;
        padding: 22px;
        font-size: 1.4rem;
        background: rgba(0,0,0,0.4);
        border: 2px solid rgba(255,255,255,0.15);
        border-radius: 20px;
        outline: none;
        transition: var(--transition);
        color: white;
        caret-color: var(--secondary);
    }

    #typing-input:focus {
        border-color: var(--primary);
        box-shadow: 0 0 0 4px rgba(67, 97, 238, 0.4);
    }

    .stats-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 25px;
        margin-top: 35px;
    }

    .stat-box {
        background: rgba(0,0,0,0.25);
        border-radius: 20px;
        padding: 25px;
        text-align: center;
        border: 1px solid rgba(255,255,255,0.08);
        box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    }

    .stat-value {
        font-size: 3rem;
        font-weight: 700;
        margin: 12px 0;
    }

    .wpm { color: var(--primary); }
    .accuracy { color: var(--success); }
    .errors { color: var(--danger); }
    #time-remaining { color: var(--secondary); }

    .controls {
        display: flex;
        justify-content: center;
        gap: 25px;
        margin-top: 40px;
        flex-wrap: wrap;
    }

    /* Videos Page */
    .videos-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
        gap: 30px;
        margin: 40px 0;
    }

    .video-card {
        background: rgba(30, 30, 46, 0.8);
        border-radius: 20px;
        overflow: hidden;
        box-shadow: var(--shadow);
        transition: var(--transition);
        border: 1px solid rgba(255,255,255,0.15);
        display: flex;
        flex-direction: column;
    }

    .video-card:hover {
        transform: translateY(-10px);
        border-color: var(--secondary);
        box-shadow: 0 15px 30px rgba(0,0,0,0.4);
    }

    .video-thumbnail {
        position: relative;
        padding-top: 56.25%;
        background-color: #000;
    }

    .video-thumbnail iframe {
        position: absolute;
        top: 0; left: 0;
        width: 100%; height: 100%;
        border: none;
    }

    .video-info {
        padding: 20px;
        flex-grow: 1;
        display: flex;
        flex-direction: column;
    }

    .video-info h3 {
        font-size: 1.5rem;
        margin-bottom: 10px;
        display: flex;
        align-items: center;
        gap: 10px;
        color: var(--light);
    }

    .video-info p {
        color: var(--gray);
        margin-bottom: 15px;
        font-size: 0.95rem;
        flex-grow: 1;
    }

    .video-meta {
        display: flex;
        justify-content: space-between;
        color: var(--gray);
        font-size: 0.85rem;
        margin-top: 10px;
    }

    .video-actions {
        margin-top: 15px;
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
    }

    .video-actions .btn {
        padding: 8px 15px;
        font-size: 0.9rem;
        border-radius: 8px;
        min-width: unset;
        width: fit-content;
        box-shadow: none;
    }

    .video-actions .btn:hover {
        transform: none;
        box-shadow: none;
    }

    /* Profile Page */
    .profile-container {
        display: grid;
        grid-template-columns: 350px 1fr;
        gap: 40px;
        margin: 40px 0;
    }

    .profile-sidebar {
        background: rgba(30, 30, 46, 0.8);
        border-radius: 25px;
        padding: 35px;
        text-align: center;
        border: 1px solid rgba(255,255,255,0.15);
        box-shadow: var(--shadow);
    }

    .profile-pic {
        width: 180px;
        height: 180px;
        border-radius: 50%;
        margin: 0 auto 25px;
        background: linear-gradient(135deg, var(--primary), var(--secondary));
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 5rem;
        color: white;
        border: 5px solid rgba(255,255,255,0.2);
        box-shadow: 0 0 0 5px var(--primary-dark);
    }

    .profile-name {
        font-size: 2.2rem;
        margin-bottom: 12px;
        color: var(--secondary);
    }

    .profile-email {
        color: var(--gray);
        margin-bottom: 25px;
        font-size: 1rem;
    }

    .profile-stats {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 20px;
        margin: 30px 0;
    }

    .profile-stat {
        background: rgba(0,0,0,0.2);
        padding: 20px;
        border-radius: 15px;
        border: 1px solid rgba(255,255,255,0.08);
    }

    .profile-stat-value {
        font-size: 2.5rem;
        font-weight: 700;
        color: var(--accent);
        margin-bottom: 5px;
    }

    .profile-stat-label {
        font-size: 1rem;
        color: var(--gray);
    }

    .profile-content {
        background: rgba(30, 30, 46, 0.8);
        border-radius: 25px;
        padding: 35px;
        border: 1px solid rgba(255,255,255,0.15);
        box-shadow: var(--shadow);
    }

    .profile-section {
        margin-bottom: 40px;
    }

    .profile-section h2 {
        font-size: 2rem;
        margin-bottom: 25px;
        padding-bottom: 15px;
        border-bottom: 2px solid var(--primary);
        color: var(--light);
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .history-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
        gap: 25px;
    }

    .history-card {
        background: rgba(0,0,0,0.25);
        border-radius: 20px;
        padding: 25px;
        border: 1px solid rgba(255,255,255,0.08);
        box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    }

    .history-card h3 {
        margin-bottom: 12px;
        color: var(--secondary);
        font-size: 1.3rem;
    }

    .history-card p {
        color: var(--gray);
        margin-bottom: 15px;
        font-size: 0.95rem;
    }

    .history-stats {
        display: flex;
        justify-content: space-between;
        font-size: 0.9rem;
        color: var(--light);
    }

    /* Footer */
    footer {
        text-align: center;
        padding: 30px 0;
        margin-top: 50px;
        border-top: 1px solid rgba(255,255,255,0.1);
    }

    .social-links {
        display: flex;
        justify-content: center;
        gap: 25px;
        margin: 25px 0;
    }

    .social-links a {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        width: 55px;
        height: 55px;
        border-radius: 50%;
        background: rgba(255,255,255,0.08);
        color: var(--light);
        font-size: 1.8rem;
        transition: var(--transition);
        border: 1px solid rgba(255,255,255,0.1);
    }

    .social-links a:hover {
        background: var(--primary);
        transform: translateY(-8px) rotate(10deg);
        box-shadow: 0 10px 20px rgba(67, 97, 238, 0.4);
    }

    /* Responsive */
    @media (max-width: 1200px) {
        .container {
            padding: 15px;
        }
    }

    @media (max-width: 900px) {
        .profile-container {
            grid-template-columns: 1fr;
        }
        .welcome-banner h1 {
            font-size: 3rem;
        }
        .welcome-banner p {
            font-size: 1.3rem;
        }
        .feature-card {
            padding: 30px;
        }
        .feature-icon {
            font-size: 3rem;
        }
        .feature-card h3 {
            font-size: 1.4rem;
        }
        .videos-container {
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        }
        nav ul {
            gap: 15px;
        }
        nav a {
            padding: 8px 12px;
            font-size: 0.95rem;
        }
    }

    @media (max-width: 768px) {
        header {
            flex-direction: column;
            gap: 15px;
        }
        nav ul {
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
        }
        nav a span {
            display: none;
        }
        nav a {
            padding: 10px;
            min-width: 45px;
            justify-content: center;
        }
        .welcome-banner {
            padding: 40px 20px;
        }
        .welcome-banner h1 {
            font-size: 2.5rem;
        }
        .welcome-banner p {
            font-size: 1.1rem;
        }
        .cta-buttons {
            flex-direction: column;
            gap: 15px;
        }
        .test-header {
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }
        .time-options {
            width: 100%;
            justify-content: center;
        }
        .stats-container {
            grid-template-columns: 1fr;
        }
        .profile-container {
            grid-template-columns: 1fr;
        }
        .history-grid {
            grid-template-columns: 1fr;
        }
        .video-card {
            flex-direction: column;
        }
        .video-thumbnail {
            width: 100%;
            height: auto;
        }
        .video-info {
            padding: 15px;
        }
        .add-video-section {
            padding: 20px;
        }
    }

    @media (max-width: 480px) {
        .logo span {
            display: none;
        }
        .logo {
            font-size: 1.5rem;
        }
        .welcome-banner h1 {
            font-size: 2rem;
        }
        .welcome-banner p {
            font-size: 1rem;
        }
        .feature-card {
            padding: 25px;
        }
        .feature-icon {
            font-size: 2.5rem;
        }
        .feature-card h3 {
            font-size: 1.2rem;
        }
        .btn {
            padding: 12px 25px;
            font-size: 1rem;
        }
        #typing-text {
            font-size: 1.3rem;
            padding: 20px;
            min-height: 180px;
        }
        #typing-input {
            padding: 18px;
            font-size: 1.2rem;
        }
        .stat-value {
            font-size: 2.2rem;
        }
        .profile-name {
            font-s
