<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adam Brousell - Data Analytics Professional</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            line-height: 1.6;
            color: #e0e0e0;
            background: #000000;
            overflow-x: hidden;
        }
        
        /* Mesh Gradient Background */
        .mesh-gradient {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(at 20% 30%, rgba(59, 130, 246, 0.15) 0px, transparent 50%),
                radial-gradient(at 80% 0%, rgba(96, 165, 250, 0.12) 0px, transparent 50%),
                radial-gradient(at 0% 50%, rgba(37, 99, 235, 0.15) 0px, transparent 50%),
                radial-gradient(at 80% 80%, rgba(71, 85, 105, 0.12) 0px, transparent 50%),
                radial-gradient(at 0% 100%, rgba(30, 58, 138, 0.15) 0px, transparent 50%);
            z-index: 0;
            animation: meshMove 20s ease infinite;
        }
        
        @keyframes meshMove {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.8; }
        }
        
        /* Particle Grid */
        .grid-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(59, 130, 246, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(59, 130, 246, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: 1;
            pointer-events: none;
        }
        
        /* Floating Data Elements */
        .data-particles {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: 2;
            pointer-events: none;
        }
        
        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: linear-gradient(45deg, #3b82f6, #60a5fa);
            border-radius: 50%;
            opacity: 0.4;
            animation: particleFloat 15s infinite ease-in-out;
        }
        
        .particle:nth-child(1) { left: 10%; top: 20%; animation-delay: 0s; }
        .particle:nth-child(2) { left: 80%; top: 40%; animation-delay: 2s; }
        .particle:nth-child(3) { left: 30%; top: 60%; animation-delay: 4s; }
        .particle:nth-child(4) { left: 70%; top: 80%; animation-delay: 6s; }
        .particle:nth-child(5) { left: 50%; top: 30%; animation-delay: 8s; }
        .particle:nth-child(6) { left: 15%; top: 75%; animation-delay: 3s; }
        .particle:nth-child(7) { left: 85%; top: 15%; animation-delay: 5s; }
        .particle:nth-child(8) { left: 25%; top: 45%; animation-delay: 7s; }
        .particle:nth-child(9) { left: 65%; top: 25%; animation-delay: 1s; }
        .particle:nth-child(10) { left: 40%; top: 85%; animation-delay: 9s; }
        .particle:nth-child(11) { left: 5%; top: 50%; animation-delay: 4.5s; }
        .particle:nth-child(12) { left: 90%; top: 60%; animation-delay: 6.5s; }
        .particle:nth-child(13) { left: 35%; top: 10%; animation-delay: 2.5s; }
        .particle:nth-child(14) { left: 75%; top: 70%; animation-delay: 8.5s; }
        .particle:nth-child(15) { left: 20%; top: 90%; animation-delay: 1.5s; }
        
        @keyframes particleFloat {
            0%, 100% { transform: translate(0, 0) scale(1); }
            33% { transform: translate(30px, -30px) scale(1.5); }
            66% { transform: translate(-30px, 30px) scale(0.8); }
        }
        
        /* Floating Graph Lines */
        .graph-line {
            position: absolute;
            opacity: 0.08;
            animation: graphFloat 40s infinite ease-in-out;
        }
        
        .graph-line svg {
            width: 500px;
            height: 200px;
        }
        
        .graph-line:nth-child(16) { 
            left: -10%; 
            top: 15%; 
            animation-delay: 0s; 
            animation-duration: 45s; 
        }
        .graph-line:nth-child(17) { 
            right: -10%; 
            top: 35%; 
            animation-delay: 8s; 
            animation-duration: 50s; 
        }
        .graph-line:nth-child(18) { 
            left: -15%; 
            bottom: 25%; 
            animation-delay: 16s; 
            animation-duration: 42s; 
        }
        .graph-line:nth-child(19) { 
            right: -10%; 
            bottom: 10%; 
            animation-delay: 24s; 
            animation-duration: 48s; 
        }
        .graph-line:nth-child(20) { 
            left: 50%; 
            top: -10%; 
            animation-delay: 32s; 
            animation-duration: 55s; 
        }
        
        @keyframes graphFloat {
            0% { 
                transform: translate(0, 0) rotate(-5deg);
                opacity: 0;
            }
            10% {
                opacity: 0.12;
            }
            50% { 
                transform: translate(120px, 100px) rotate(5deg);
                opacity: 0.15;
            }
            90% {
                opacity: 0.12;
            }
            100% { 
                transform: translate(240px, 200px) rotate(-3deg);
                opacity: 0;
            }
        }
        
        .graph-path {
            fill: none;
            stroke: #3b82f6;
            stroke-width: 2;
            stroke-linecap: round;
            stroke-dasharray: 5 5;
            animation: dashMove 3s linear infinite;
        }
        
        @keyframes dashMove {
            0% { stroke-dashoffset: 0; }
            100% { stroke-dashoffset: 20; }
        }
        
        /* Floating Geometric Shapes */
        .geo-shape {
            position: absolute;
            opacity: 0.06;
            animation: shapeFloat 35s infinite ease-in-out;
        }
        
        .geo-triangle {
            width: 0;
            height: 0;
            border-left: 60px solid transparent;
            border-right: 60px solid transparent;
            border-bottom: 100px solid rgba(59, 130, 246, 0.3);
            border-top: none;
        }
        
        .geo-hexagon {
            width: 80px;
            height: 140px;
            background: rgba(59, 130, 246, 0.15);
            position: relative;
            clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
        }
        
        /* Data-Centric Shapes */
        .bell-curve {
            width: 200px;
            height: 120px;
        }
        
        .bell-path {
            fill: none;
            stroke: #3b82f6;
            stroke-width: 2;
            opacity: 0.4;
        }
        
        .bar-chart-shape {
            display: flex;
            align-items: flex-end;
            gap: 8px;
            height: 100px;
            width: 150px;
        }
        
        .bar-item {
            flex: 1;
            background: linear-gradient(to top, rgba(59, 130, 246, 0.3), rgba(96, 165, 250, 0.2));
            border-radius: 3px 3px 0 0;
        }
        
        .scatter-plot {
            width: 120px;
            height: 120px;
            position: relative;
        }
        
        .scatter-dot {
            position: absolute;
            width: 6px;
            height: 6px;
            background: #3b82f6;
            border-radius: 50%;
            opacity: 0.4;
        }
        
        .shape-1 { left: 8%; top: 12%; animation-delay: 0s; animation-duration: 38s; }
        .shape-2 { right: 12%; top: 22%; animation-delay: 5s; animation-duration: 42s; }
        .shape-3 { left: 18%; bottom: 18%; animation-delay: 10s; animation-duration: 36s; }
        .shape-4 { right: 8%; bottom: 28%; animation-delay: 15s; animation-duration: 40s; }
        .shape-5 { left: 45%; top: 8%; animation-delay: 20s; animation-duration: 44s; }
        .shape-6 { right: 35%; bottom: 12%; animation-delay: 25s; animation-duration: 39s; }
        .shape-7 { left: 25%; top: 45%; animation-delay: 12s; animation-duration: 41s; }
        .shape-8 { right: 22%; top: 58%; animation-delay: 18s; animation-duration: 37s; }
        
        @keyframes shapeFloat {
            0%, 100% { 
                transform: translate(0, 0) rotate(0deg);
                opacity: 0.06;
            }
            25% {
                transform: translate(30px, -40px) rotate(15deg);
                opacity: 0.10;
            }
            50% { 
                transform: translate(60px, -20px) rotate(-10deg);
                opacity: 0.08;
            }
            75% {
                transform: translate(30px, 20px) rotate(8deg);
                opacity: 0.10;
            }
        }
        
        /* Content Wrapper */
        .content {
            position: relative;
            z-index: 10;
        }
        
        /* Hero Section */
        header {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            text-align: center;
            padding: 1rem;
            max-width: 1200px;
            z-index: 2;
        }
        
        .hero-badge {
            display: inline-block;
            padding: 0.25rem 0.75rem;
            background: rgba(59, 130, 246, 0.1);
            border: 1px solid rgba(59, 130, 246, 0.3);
            border-radius: 50px;
            color: #93c5fd;
            font-size: 0.875rem;
            font-weight: 600;
            letter-spacing: 0.5px;
            margin-bottom: 2rem;
            backdrop-filter: blur(10px);
        }
        
        h1 {
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 900;
            margin-bottom: .5rem;
            background: linear-gradient(135deg, #ffffff 0%, #93c5fd 50%, #60a5fa 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            line-height: 1.1;
            letter-spacing: -2px;
        }
        
        .hero-subtitle {
            font-size: clamp(1.25rem, 3vw, 1.75rem);
            color: #9ca3af;
            margin-bottom: 1rem;
            font-weight: 400;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: .5rem 1.25rem;
            border-radius: 12px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            font-size: 1.1rem;
            display: inline-block;
        }
        
        .btn-primary {
            background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
            color: white;
            box-shadow: 0 10px 40px rgba(59, 130, 246, 0.3);
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 50px rgba(59, 130, 246, 0.4);
        }
        
        .btn-secondary {
            background: rgba(255, 255, 255, 0.05);
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }
        
        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: rgba(255, 255, 255, 0.2);
        }
        
        /* Navigation */
        nav {
            position: fixed;
            top: 2rem;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(17, 24, 39, 0.8);
            backdrop-filter: blur(20px);
            padding: .5rem 1rem;
            border-radius: 50px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            z-index: 1000;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
        }
        
        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }
        
        nav a {
            color: #9ca3af;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: #fff;
        }
        
        /* Sections */
        section {
            padding: 1rem .5rem;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .section-header {
            text-align: center;
            margin-bottom: 1rem;
        }
        
        .section-tag {
            display: inline-block;
            padding: 0.5rem 1.5rem;
            background: rgba(59, 130, 246, 0.1);
            border: 1px solid rgba(59, 130, 246, 0.3);
            border-radius: 50px;
            color: #93c5fd;
            font-size: 0.875rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }
        
        h2 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #ffffff 0%, #93c5fd 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .section-description {
            font-size: 1.25rem;
            color: #9ca3af;
            max-width: 700px;
            margin: 0 auto;
        }
        
        /* Bento Grid */
        .bento-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 1rem;
        }
        
        .bento-card {
            background: rgba(17, 24, 39, 0.5);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 24px;
            padding: 1rem;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .bento-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(30, 64, 175, 0.1) 100%);
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .bento-card:hover {
            transform: translateY(-8px);
            border-color: rgba(59, 130, 246, 0.3);
            box-shadow: 0 20px 60px rgba(59, 130, 246, 0.2);
        }
        
        .bento-card:hover::before {
            opacity: 1;
        }
        
        .card-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            display: block;
        }
        
        .bento-card h3 {
            font-size: 1.5rem;
            font-weight: 700;
            color: white;
            margin-bottom: 1rem;
            position: relative;
            z-index: 1;
        }
        
        .bento-card p, .bento-card ul {
            color: #9ca3af;
            line-height: 1.8;
            position: relative;
            z-index: 1;
        }
        
        .bento-card ul {
            list-style: none;
        }
        
        .bento-card li {
            padding: 0.5rem 0;
            padding-left: 1.5rem;
            position: relative;
        }
        
        .bento-card li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: #3b82f6;
            font-weight: bold;
        }
        
        /* Large Feature Cards */
        .feature-large {
            grid-column: span 2;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(30, 64, 175, 0.1) 100%);
            display: flex;
            align-items: center;
            gap: 3rem;
            padding: 3rem;
        }
        
        .feature-image {
            flex: 1;
            min-width: 300px;
            height: 300px;
            background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
            border-radius: 20px;
            position: relative;
            overflow: hidden;
        }
        
        .feature-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 0.9;
            mix-blend-mode: luminosity;
        }
        
        .feature-content {
            flex: 1;
        }
        
        /* Timeline */
        .timeline {
            position: relative;
            padding-left: 3rem;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 2px;
            background: linear-gradient(to bottom, #3b82f6, #1e40af);
        }
        
        .timeline-item {
            position: relative;
            margin-bottom: 3rem;
            padding-left: 2rem;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -3.5rem;
            top: 0;
            width: 12px;
            height: 12px;
            background: #3b82f6;
            border-radius: 50%;
            box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.2);
        }
        
        .timeline-date {
            color: #60a5fa;
            font-weight: 600;
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }
        
        .timeline-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: white;
            margin-bottom: 0.5rem;
        }
        
        .timeline-company {
            color: #93c5fd;
            font-weight: 600;
            margin-bottom: 1rem;
        }
        
        .timeline-description {
            color: #9ca3af;
            line-height: 1.8;
        }
        
        /* Project Cards */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            background: rgba(17, 24, 39, 0.5);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 24px;
            overflow: hidden;
            transition: all 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-8px);
            border-color: rgba(59, 130, 246, 0.3);
            box-shadow: 0 20px 60px rgba(59, 130, 246, 0.2);
        }
        
        .project-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
            position: relative;
            overflow: hidden;
        }
        
        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 0.8;
            mix-blend-mode: luminosity;
        }
        
        .project-content {
            padding: 2rem;
        }
        
        .project-content h4 {
            font-size: 1.5rem;
            font-weight: 700;
            color: white;
            margin-bottom: 1rem;
        }
        
        .project-content p {
            color: #9ca3af;
            line-height: 1.8;
        }
        
        /* Stats Section */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .stat-card {
            text-align: center;
            padding: 2rem;
            background: rgba(59, 130, 246, 0.1);
            border: 1px solid rgba(59, 130, 246, 0.2);
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: 900;
            background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .stat-label {
            color: #9ca3af;
            font-size: 1rem;
            margin-top: 0.5rem;
        }
        
        /* Footer */
        footer {
            padding: 2rem 1rem;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            margin-top: 6rem;
        }
        
        footer p {
            color: #6b7280;
        }
        
        @media (max-width: 768px) {
            nav {
                padding: 0.75rem 1.5rem;
            }
            
            nav ul {
                gap: 1rem;
            }
            
            .feature-large {
                grid-column: span 1;
                flex-direction: column;
            }
            
            .timeline {
                padding-left: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Background Elements -->
    <div class="mesh-gradient"></div>
    <div class="grid-overlay"></div>
    <div class="data-particles">
        <!-- Data Points -->
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        
        <!-- Floating Graph Lines -->
        <div class="graph-line">
            <svg viewBox="0 0 500 200">
                <path class="graph-path" d="M 10,120 Q 80,40 150,90 T 300,70 T 450,100"/>
            </svg>
        </div>
        <div class="graph-line">
            <svg viewBox="0 0 500 200">
                <path class="graph-path" d="M 10,100 Q 100,150 180,110 T 350,80 T 490,130"/>
            </svg>
        </div>
        <div class="graph-line">
            <svg viewBox="0 0 500 200">
                <path class="graph-path" d="M 10,60 Q 120,110 200,80 T 360,100 T 490,50"/>
            </svg>
        </div>
        <div class="graph-line">
            <svg viewBox="0 0 500 200">
                <path class="graph-path" d="M 10,140 Q 90,70 170,120 T 320,90 T 480,130"/>
            </svg>
        </div>
        <div class="graph-line">
            <svg viewBox="0 0 500 200">
                <path class="graph-path" d="M 10,90 Q 110,30 190,70 T 340,110 T 490,60"/>
            </svg>
        </div>
        
        <!-- Floating Geometric Shapes -->
        <div class="geo-shape bell-curve shape-1">
            <svg viewBox="0 0 200 120">
                <path class="bell-path" d="M 10,110 Q 50,110 70,80 Q 100,20 130,80 Q 150,110 190,110"/>
            </svg>
        </div>
        
        <div class="geo-shape bar-chart-shape shape-2">
            <div class="bar-item" style="height: 50%;"></div>
            <div class="bar-item" style="height: 75%;"></div>
            <div class="bar-item" style="height: 90%;"></div>
            <div class="bar-item" style="height: 65%;"></div>
            <div class="bar-item" style="height: 80%;"></div>
        </div>
        
        <div class="geo-shape geo-hexagon shape-3"></div>
        
        <div class="geo-shape scatter-plot shape-4">
            <div class="scatter-dot" style="left: 20%; top: 60%;"></div>
            <div class="scatter-dot" style="left: 35%; top: 45%;"></div>
            <div class="scatter-dot" style="left: 50%; top: 30%;"></div>
            <div class="scatter-dot" style="left: 65%; top: 50%;"></div>
            <div class="scatter-dot" style="left: 80%; top: 35%;"></div>
            <div class="scatter-dot" style="left: 25%; top: 75%;"></div>
            <div class="scatter-dot" style="left: 70%; top: 65%;"></div>
            <div class="scatter-dot" style="left: 45%; top: 55%;"></div>
        </div>
        
        <div class="geo-shape bell-curve shape-5">
            <svg viewBox="0 0 200 120">
                <path class="bell-path" d="M 10,110 Q 50,110 70,80 Q 100,20 130,80 Q 150,110 190,110"/>
            </svg>
        </div>
        
        <div class="geo-shape bar-chart-shape shape-6">
            <div class="bar-item" style="height: 60%;"></div>
            <div class="bar-item" style="height: 85%;"></div>
            <div class="bar-item" style="height: 70%;"></div>
            <div class="bar-item" style="height: 95%;"></div>
            <div class="bar-item" style="height: 55%;"></div>
        </div>
        
        <div class="geo-shape geo-triangle shape-7"></div>
        
        <div class="geo-shape scatter-plot shape-8">
            <div class="scatter-dot" style="left: 15%; top: 70%;"></div>
            <div class="scatter-dot" style="left: 30%; top: 40%;"></div>
            <div class="scatter-dot" style="left: 55%; top: 25%;"></div>
            <div class="scatter-dot" style="left: 70%; top: 55%;"></div>
            <div class="scatter-dot" style="left: 85%; top: 45%;"></div>
            <div class="scatter-dot" style="left: 40%; top: 80%;"></div>
            <div class="scatter-dot" style="left: 60%; top: 60%;"></div>
        </div>
    </div>
    
    <!-- Navigation -->
            <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#certifications">Certifications</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    
    <!-- Content -->
    <div class="content">
        <!-- Hero Section -->
        <header>
            <div class="hero-content">
                <div class="hero-badge">DATA DRIVEN PROFESSIONAL</div>
                <h1>Adam Brousell</h1>
                <p class="hero-subtitle">Transforming 15+ years of operations expertise into data-driven insights. Specialized in supply chain analytics, business intelligence, and operational optimization.</p>
                <div class="cta-buttons">
                    <a href="#contact" class="btn btn-primary">Get In Touch</a>
                    <a href="#projects" class="btn btn-secondary">View Projects</a>
                </div>
            </div>
        </header>
        
        <!-- About Section -->
        <section id="about">
            <div class="section-header">
                <div class="section-tag">WHO I AM</div>
                <h2>Bridging Operations & Analytics</h2>
                <p class="section-description">I combine deep operational expertise with modern analytics tools to turn complex data into actionable business insights.</p>
            </div>
            
            <div class="bento-grid">
                <div class="bento-card feature-large">
                    <div class="feature-image">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=800&h=600&fit=crop" alt="Data Analytics Dashboard">
                    </div>
                    <div class="feature-content">
                        <h3>From Operations to Analytics</h3>
                        <p>With a Bachelor of Science in Supply Chain Management from Lehigh University and Google Data Analytics certification, I've spent 15+ years managing high-volume restaurant operations while developing expertise in data analysis, forecasting, and business intelligence.</p>
                        <p style="margin-top: 1rem;">My unique background combines P&L ownership, inventory optimization, and people analytics with technical proficiency in Excel, SQL, and Power BI.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Skills Section -->
        <section id="skills">
            <div class="section-header">
                <div class="section-tag">EXPERTISE</div>
                <h2>Technical Skills</h2>
            </div>
            
            <div class="bento-grid">
                <div class="bento-card">
                    <span class="card-icon">📊</span>
                    <h3>Data Analysis</h3>
                    <ul>
                        <li>Microsoft Excel (Advanced)</li>
                        <li>SQL Querying</li>
                        <li>Power BI Dashboards</li>
                        <li>Data Visualization</li>
                        <li>Statistical Analysis</li>
                    </ul>
                </div>
                
                <div class="bento-card">
                    <span class="card-icon">⚙️</span>
                    <h3>Operations</h3>
                    <ul>
                        <li>Supply Chain Management</li>
                        <li>Process Optimization</li>
                        <li>Inventory Control</li>
                        <li>Vendor Management</li>
                        <li>Cost Reduction</li>
                    </ul>
                </div>
                
                <div class="bento-card">
                    <span class="card-icon">📈</span>
                    <h3>Business Analytics</h3>
                    <ul>
                        <li>KPI Development</li>
                        <li>Performance Metrics</li>
                        <li>Forecasting Models</li>
                        <li>People Analytics</li>
                        <li>Business Intelligence</li>
                    </ul>
                </div>
                
                <div class="bento-card">
                    <span class="card-icon">👥</span>
                    <h3>Leadership</h3>
                    <ul>
                        <li>Team Management</li>
                        <li>P&L Ownership</li>
                        <li>Strategic Planning</li>
                        <li>Stakeholder Communication</li>
                        <li>Cross-functional Collaboration</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <!-- Education Section -->
        <section id="education">
            <div class="section-header">
                <div class="section-tag">EDUCATION</div>
                <h2>Academic Background</h2>
            </div>
            
            <div class="timeline">
                <div class="timeline-item" style="border-bottom: none; padding-bottom: 0;">
                    <div class="timeline-date">DEC 2007</div>
                    <div class="timeline-title">Bachelor of Science in Supply Chain Management</div>
                    <div class="timeline-company">Lehigh University | Bethlehem, PA</div>
                </div>
            </div>
        </section>
        
        <!-- Certifications Section -->
        <section id="certifications">
            <div class="section-header">
                <div class="section-tag">CERTIFICATIONS</div>
                <h2>Professional Development</h2>
            </div>
            
            <div class="timeline">
                <div class="timeline-item" style="border-bottom: none; padding-bottom: 0;">
                    <div class="timeline-date">2024</div>
                    <div class="timeline-title">Google Data Analytics Professional Certificate</div>
                    <div class="timeline-company">Google (via Coursera)</div>
                </div>
            </div>
        </section>
        
        <!-- Experience Section -->
        <section id="experience">
            <div class="section-header">
                <div class="section-tag">CAREER PATH</div>
                <h2>Professional Journey</h2>
            </div>
            
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-date">DEC 2010 - DEC 2025</div>
                    <div class="timeline-title">General Manager / Restaurant Operations Manager</div>
                    <div class="timeline-company">Multiple Full-Service Restaurants | Monmouth County, NJ</div>
                    <p class="timeline-description" style="font-style: italic; margin-bottom: 1rem;">Tre Pizza • Taka Japanese Bar • Stella Marina • Fresh • Dolce Fantasia • Nanna's Kitchen</p>
                    <p class="timeline-description"><strong>Core Focus:</strong> KPI ownership, budgeting & P&L exposure, labor forecasting, process improvement, vendor & inventory management</p>
                    <ul style="margin-top: 1rem; list-style: none; color: #9ca3af;">
                        <li style="padding: 0.3rem 0;">→ Led end-to-end operations and inventory management for high-volume environments</li>
                        <li style="padding: 0.3rem 0;">→ Managed 50-60+ employees, aligning workforce with demand patterns</li>
                        <li style="padding: 0.3rem 0;">→ Analyzed sales trends and seasonal patterns for forecasting and optimization</li>
                        <li style="padding: 0.3rem 0;">→ Reduced waste and stockouts through improved inventory controls</li>
                        <li style="padding: 0.3rem 0;">→ Executed weekly payroll and labor cost tracking for budget management</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-date">FEB 2008 - JAN 2010</div>
                    <div class="timeline-title">Staff Accountant</div>
                    <div class="timeline-company">KML & Associates, LLC | Little Silver, NJ</div>
                    <ul style="margin-top: 1rem; list-style: none; color: #9ca3af;">
                        <li style="padding: 0.3rem 0;">→ Prepared personal and business tax returns for federal and state agencies</li>
                        <li style="padding: 0.3rem 0;">→ Assisted with audit engagements for large multi-national commercial banks</li>
                        <li style="padding: 0.3rem 0;">→ Conducted independent physical inventory audits to verify record integrity</li>
                        <li style="padding: 0.3rem 0;">→ Field examiner for commercial loan examination services</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-date">MAR 2004 - SEP 2007</div>
                    <div class="timeline-title">Ride Operations Supervisor</div>
                    <div class="timeline-company">Six Flags Great Adventure Resort | Jackson, NJ</div>
                    <ul style="margin-top: 1rem; list-style: none; color: #9ca3af;">
                        <li style="padding: 0.3rem 0;">→ Directed, motivated, trained, scheduled, and audited a professional staff of 50+ in a fast-paced service environment</li>
                        <li style="padding: 0.3rem 0;">→ Enhanced customer experience by creating an environment emphasizing safety and motivating employees through strategic position rotation and workload balancing</li>
                        <li style="padding: 0.3rem 0;">→ Ensured smooth operations while enforcing safety regulations through continuous communication with supervisors and routine safety procedures</li>
                        <li style="padding: 0.3rem 0;">→ Performed critical first responder role during emergency situations, coordinating employee evacuations and conferring with maintenance personnel</li>
                        <li style="padding: 0.3rem 0;">→ Auditing Supervisor: Led newly created task force to target deficiencies in training of front-line workers in Rides Department (2007)</li>
                    </ul>
                </div>
            </div>
        </section>
        
              
        <!-- Projects Section -->
        <section id="projects">
            <div class="section-header">
                <div class="section-tag">PORTFOLIO</div>
                <h2>Featured Projects</h2>
            </div>
            
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=600&h=400&fit=crop" alt="Power BI Dashboard">
                    </div>
                    <div class="project-content">
                        <h4>Restaurant Performance Dashboard</h4>
                        <p>Designed interactive Power BI dashboard tracking daily sales, labor costs, and food waste metrics. Enabled data-driven staffing and menu decisions, reducing waste by 15%.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?w=600&h=400&fit=crop" alt="SQL Analysis">
                    </div>
                    <div class="project-content">
                        <h4>Supply Chain Analysis</h4>
                        <p>Analyzed vendor delivery performance and pricing data using SQL queries and Excel pivot tables. Identified cost-saving opportunities reducing procurement expenses by 12% annually.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=600&h=400&fit=crop" alt="Excel Model">
                    </div>
                    <div class="project-content">
                        <h4>Employee Scheduling Optimization</h4>
                        <p>Built Excel-based scheduling model using historical sales data and labor requirements. Optimized staff allocation to match demand patterns, improving labor efficiency by 18%.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1543286386-2e659306cd6c?w=600&h=400&fit=crop" alt="Forecasting Model">
                    </div>
                    <div class="project-content">
                        <h4>Inventory Forecasting Model</h4>
                        <p>Created predictive model for inventory ordering based on seasonal trends and historical consumption data. Reduced stockouts by 25% while minimizing excess inventory.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Contact Section -->
        <section id="contact">
            <div class="section-header">
                <div class="section-tag">LET'S CONNECT</div>
                <h2>Get In Touch</h2>
                <p class="section-description">Ready to bring analytical rigor and operational expertise to your team. Let's discuss how I can drive data-informed decisions and measurable results.</p>
            </div>
            
            <div class="cta-buttons" style="margin-top: 3rem;">
                <a href="mailto:admin@adamb.info" class="btn btn-primary">Email Me</a>
                <a href="https://linkedin.com/in/yourprofile" class="btn btn-secondary" target="_blank">LinkedIn</a>
            </div>
        </section>
        
        <!-- Footer -->
        <footer>
            <p>&copy; 2026 Adam Brousell. All rights reserved.</p>
        </footer>
    </div>
</body>
</html>
