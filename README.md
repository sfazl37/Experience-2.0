<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Experience Personas: Designing Solutions with Empathy</title>
    <style>
        :root {
            --primary-color: #2c5282;
            --secondary-color: #4299e1;
            --accent-color: #f56565;
            --text-color: #2d3748;
            --light-bg: #f7fafc;
            --card-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-bg);
            color: var(--text-color);
            line-height: 1.6;
        }
        
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 2rem;
            text-align: center;
            box-shadow: var(--card-shadow);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .slide-navigation {
            display: flex;
            justify-content: center;
            margin: 2rem 0;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .nav-button {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .nav-button:hover {
            background-color: var(--secondary-color);
        }
        
        .nav-button.active {
            background-color: var(--accent-color);
        }
        
        .slide {
            display: none;
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: var(--card-shadow);
            margin-bottom: 2rem;
        }
        
        .slide.active {
            display: block;
            animation: fadeIn 0.5s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .slide-title {
            color: var(--primary-color);
            margin-bottom: 1rem;
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 0.5rem;
        }
        
        .slide-subtitle {
            color: var(--secondary-color);
            margin-bottom: 1.5rem;
            font-style: italic;
        }
        
        .slide-content {
            margin-bottom: 1.5rem;
        }
        
        ul, ol {
            padding-left: 2rem;
            margin-bottom: 1rem;
        }
        
        .persona-card {
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            padding: 1.5rem;
            margin: 1.5rem 0;
            background-color: #f8fafc;
            box-shadow: var(--card-shadow);
        }
        
        .persona-header {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .persona-image {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background-color: #cbd5e0;
            margin-right: 1rem;
            overflow: hidden;
        }
        
        .persona-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .persona-quote {
            font-style: italic;
            background-color: #e6fffa;
            border-left: 4px solid var(--secondary-color);
            padding: 1rem;
            margin: 1rem 0;
        }
        
        .journey-map {
            display: flex;
            justify-content: space-between;
            margin: 2rem 0;
            flex-wrap: wrap;
        }
        
        .journey-step {
            flex: 1;
            min-width: 120px;
            text-align: center;
            padding: 1rem;
            margin: 0.5rem;
            background-color: #ebf8ff;
            border-radius: 8px;
            position: relative;
        }
        
        .journey-step::after {
            content: "→";
            position: absolute;
            right: -10px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 1.5rem;
            color: var(--secondary-color);
        }
        
        .journey-step:last-child::after {
            display: none;
        }
        
        .emotion {
            display: inline-block;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            margin-top: 0.5rem;
        }
        
        .emotion.positive {
            background-color: #48bb78;
        }
        
        .emotion.neutral {
            background-color: #ecc94b;
        }
        
        .emotion.negative {
            background-color: #e53e3e;
        }
        
        .timeline {
            display: flex;
            justify-content: space-between;
            margin: 2rem 0;
            position: relative;
        }
        
        .timeline::before {
            content: "";
            position: absolute;
            top: 15px;
            left: 0;
            right: 0;
            height: 2px;
            background-color: var(--secondary-color);
            z-index: 1;
        }
        
        .timeline-point {
            position: relative;
            z-index: 2;
            text-align: center;
            flex: 1;
        }
        
        .timeline-marker {
            width: 30px;
            height: 30px;
            background-color: var(--primary-color);
            border-radius: 50%;
            margin: 0 auto 0.5rem;
        }
        
        .timeline-date {
            font-size: 0.85rem;
            font-weight: bold;
        }
        
        .compare-table {
            width: 100%;
            border-collapse: collapse;
            margin: 1.5rem 0;
        }
        
        .compare-table th, .compare-table td {
            border: 1px solid #e2e8f0;
            padding: 0.75rem;
            text-align: left;
        }
        
        .compare-table th {
            background-color: var(--primary-color);
            color: white;
        }
        
        .compare-table tr:nth-child(even) {
            background-color: #f7fafc;
        }
        
        .button-container {
            display: flex;
            justify-content: space-between;
            margin-top: 2rem;
        }
        
        .prev-button, .next-button {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 0.75rem 1.5rem;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
            font-size: 1rem;
        }
        
        .prev-button:hover, .next-button:hover {
            background-color: var(--secondary-color);
        }
        
        .prev-button:disabled, .next-button:disabled {
            background-color: #cbd5e0;
            cursor: not-allowed;
        }
        
        footer {
            text-align: center;
            padding: 2rem;
            background-color: var(--primary-color);
            color: white;
            margin-top: 2rem;
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            
            .journey-map {
                flex-direction: column;
            }
            
            .journey-step::after {
                content: "↓";
                right: 50%;
                bottom: -15px;
                top: auto;
                transform: translateX(50%);
            }
            
            .timeline {
                flex-direction: column;
            }
            
            .timeline::before {
                top: 0;
                bottom: 0;
                left: 15px;
                right: auto;
                width: 2px;
                height: auto;
            }
            
            .timeline-point {
                display: flex;
                align-items: center;
                margin-bottom: 1rem;
            }
            
            .timeline-marker {
                margin: 0 1rem 0 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Experience Personas: Designing Solutions with Empathy</h1>
        <p>Using data-driven personas to enhance workplace experience delivery</p>
    </header>
    
    <div class="container">
        <div class="slide-navigation">
            <button class="nav-button active" onclick="showSlide(0)">Intro</button>
            <button class="nav-button" onclick="showSlide(1)">What Are Personas</button>
            <button class="nav-button" onclick="showSlide(2)">Business Case</button>
            <button class="nav-button" onclick="showSlide(3)">Key Elements 1</button>
            <button class="nav-button" onclick="showSlide(4)">Key Elements 2</button>
            <button class="nav-button" onclick="showSlide(5)">Meet Aman</button>
            <button class="nav-button" onclick="showSlide(6)">Aman's Experience</button>
            <button class="nav-button" onclick="showSlide(7)">Implementation 1</button>
            <button class="nav-button" onclick="showSlide(8)">Implementation 2</button>
            <button class="nav-button" onclick="showSlide(9)">Next Steps</button>
            <button class="nav-button" onclick="showSlide(10)">Q&A</button>
        </div>
        
        <!-- Slide 1: Title -->
        <div class="slide active" id="slide-0">
            <h2 class="slide-title">Experience Personas: Designing Solutions with Empathy</h2>
            <h3 class="slide-subtitle">Using data-driven personas to enhance workplace experience delivery</h3>
            
            <div class="slide-content">
                <div style="height: 300px; background-color: #e2e8f0; display: flex; align-items: center; justify-content: center; border-radius: 8px; margin-bottom: 1rem;">
                    <p>[Placeholder for image: Diverse workplace with multiple employee types interacting]</p>
                </div>
                <p>Welcome to our presentation on Experience Personas. Today we'll explore how creating research-based personas can transform our approach to workplace experience design and delivery.</p>
            </div>
            
            <div class="button-container">
                <button class="prev-button" disabled>Previous</button>
                <button class="next-button" onclick="nextSlide()">Next</button>
            </div>
        </div>
        
        <!-- Slide 2: Understanding Experience Personas -->
        <div class="slide" id="slide-1">
            <h2 class="slide-title">What Are Experience Personas?</h2>
            
            <div class="slide-content">
                <ul>
                    <li><strong>Definition:</strong> Research-based representations of employee archetypes that capture behaviors, needs, and pain points</li>
                    <li><strong>Purpose:</strong> To move beyond demographic segmentation toward motivation and experience-based understanding</li>
                    <li><strong>Foundation:</strong> Built using qualitative interviews, surveys, observation data, and usage analytics</li>
                </ul>
                
                <div class="persona-card">
                    <div style="text-align: center; margin-bottom: 1rem;">
                        <p>[Example persona card with key elements highlighted]</p>
                    </div>
                    <p>Personas transform raw data into actionable insights by creating realistic representations of your employees that the entire organization can understand and relate to.</p>
                </div>
            </div>
            
            <div class="button-container">
                <button class="prev-button" onclick="prevSlide()">Previous</button>
                <button class="next-button" onclick="nextSlide()">Next</button>
            </div>
        </div>
        
        <!-- Slide 3: The Business Case -->
        <div class="slide" id="slide-2">
            <h2 class="slide-title">Why Experience Personas Matter</h2>
            
            <div class="slide-content">
                <ul>
                    <li>Prevent one-size-fits-all solutions that satisfy no one completely</li>
                    <li>Enable empathetic design thinking across all experience touchpoints</li>
                    <li>Allow for targeted communications and interventions</li>
                    <li>Help Enablers anticipate needs before they become problems</li>
                </ul>
                
                <table class="compare-table">
                    <thead>
                        <tr>
                            <th>Traditional Approach</th>
                            <th>Persona-Based Approach
