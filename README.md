
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deborah Nyanchama | Digital Marketing Strategist</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-navy: #1A2A40;
            --accent-amber: #FFB400;
            --accent-coral: #E94E3C;
            --neutral-warm: #F5F5F5;
            --highlight-sage: #4CAF50;
            --white: #FFFFFF;
            --text-dark: #2D3748;
            --text-light: #718096;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--neutral-warm);
            color: var(--text-dark);
            line-height: 1.6;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 600;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: var(--primary-navy);
            padding: 1rem 5%;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(26, 42, 64, 0.3);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2.5rem;
        }

        nav a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.9rem;
            transition: color 0.3s;
            position: relative;
        }

        nav a:hover {
            color: var(--accent-amber);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent-amber);
            transition: width 0.3s;
        }

        nav a:hover::after {
            width: 100%;
        }

        /* Cover Section */
        .cover-section {
            min-height: 100vh;
            background: linear-gradient(135deg, var(--primary-navy) 0%, #2d3e50 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            padding: 2rem;
        }

        .geometric-shapes {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .shape {
            position: absolute;
            opacity: 0.1;
        }

        .shape-1 {
            width: 300px;
            height: 300px;
            border: 3px solid var(--accent-amber);
            border-radius: 50%;
            top: -100px;
            right: -50px;
            animation: float 6s ease-in-out infinite;
        }

        .shape-2 {
            width: 200px;
            height: 200px;
            background: var(--accent-coral);
            transform: rotate(45deg);
            bottom: -50px;
            left: -50px;
            opacity: 0.15;
        }

        .shape-3 {
            width: 150px;
            height: 150px;
            border: 2px solid var(--highlight-sage);
            bottom: 20%;
            right: 10%;
            transform: rotate(15deg);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .cover-content {
            text-align: center;
            z-index: 10;
            max-width: 900px;
        }

        .cover-badge {
            display: inline-block;
            background: var(--accent-amber);
            color: var(--primary-navy);
            padding: 0.5rem 1.5rem;
            font-weight: 700;
            font-size: 0.85rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 2rem;
            border-radius: 2px;
        }

        .cover-content h1 {
            font-size: 4rem;
            color: var(--white);
            margin-bottom: 1rem;
            letter-spacing: -1px;
        }

        .cover-content .title {
            font-size: 1.5rem;
            color: var(--accent-amber);
            font-weight: 300;
            margin-bottom: 2rem;
            letter-spacing: 3px;
        }

        .cover-tagline {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.8);
            max-width: 600px;
            margin: 0 auto 3rem;
            font-weight: 300;
        }

        .cover-stats {
            display: flex;
            justify-content: center;
            gap: 4rem;
            margin-top: 3rem;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            color: var(--accent-coral);
            display: block;
            font-family: 'Playfair Display', serif;
        }

        .stat-label {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Section Styling */
        section {
            padding: 5rem 10%;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-header h2 {
            font-size: 2.5rem;
            color: var(--primary-navy);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .section-header h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: var(--accent-coral);
        }

        .section-header p {
            color: var(--text-light);
            max-width: 600px;
            margin: 1.5rem auto 0;
        }

        /* Professional Summary */
        .summary-section {
            background: var(--white);
        }

        .summary-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .summary-text {
            font-size: 1.1rem;
            line-height: 1.8;
            color: var(--text-dark);
        }

        .summary-text p {
            margin-bottom: 1.5rem;
        }

        .highlight-box {
            background: var(--primary-navy);
            color: var(--white);
            padding: 2rem;
            border-left: 5px solid var(--accent-amber);
            margin: 2rem 0;
        }

        .highlight-box p {
            font-style: italic;
            font-size: 1.2rem;
            margin: 0;
        }

        .summary-image {
            position: relative;
        }

        .summary-image img {
            width: 100%;
            border-radius: 4px;
            box-shadow: 0 20px 40px rgba(26, 42, 64, 0.2);
        }

        /* Skills Section */
        .skills-section {
            background: var(--neutral-warm);
        }

        .skills-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
        }

        .skill-card {
            background: var(--white);
            padding: 2.5rem;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s, box-shadow 0.3s;
            border-top: 4px solid var(--accent-amber);
        }

        .skill-card:nth-child(2) {
            border-top-color: var(--accent-coral);
        }

        .skill-card:nth-child(3) {
            border-top-color: var(--highlight-sage);
        }

        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.12);
        }

        .skill-icon {
            width: 60px;
            height: 60px;
            background: var(--primary-navy);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.5rem;
            color: var(--accent-amber);
            font-size: 1.5rem;
        }

        .skill-card h3 {
            color: var(--primary-navy);
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            padding: 0.5rem 0;
            border-bottom: 1px solid #eee;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .skill-list li::before {
            content: '▸';
            color: var(--accent-coral);
            font-weight: bold;
        }

        /* Experience Section */
        .experience-section {
            background: var(--white);
        }

        .exp-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .exp-item {
            display: flex;
            gap: 3rem;
            margin-bottom: 4rem;
            padding-bottom: 4rem;
            border-bottom: 2px solid var(--neutral-warm);
        }

        .exp-item:last-child {
            border-bottom: none;
        }

        .exp-timeline {
            flex-shrink: 0;
            width: 80px;
            text-align: center;
        }

        .exp-dot {
            width: 20px;
            height: 20px;
            background: var(--accent-coral);
            border-radius: 50%;
            margin: 0 auto 1rem;
            position: relative;
        }

        .exp-dot::after {
            content: '';
            position: absolute;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100px;
            background: var(--accent-amber);
        }

        .exp-content h3 {
            color: var(--primary-navy);
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .exp-content .role {
            color: var(--accent-coral);
            font-weight: 600;
            margin-bottom: 1rem;
            display: block;
        }

        .exp-content p {
            color: var(--text-light);
            margin-bottom: 1rem;
        }

        .exp-achievements {
            list-style: none;
            margin-top: 1.5rem;
        }

        .exp-achievements li {
            padding: 0.8rem 0;
            padding-left: 2rem;
            position: relative;
            border-left: 3px solid var(--highlight-sage);
            margin-bottom: 0.5rem;
            background: var(--neutral-warm);
            padding: 1rem 1rem 1rem 2rem;
        }

        /* Case Study Section */
        .casestudy-section {
            background: var(--neutral-warm);
        }

        .casestudy-hero {
            background: linear-gradient(135deg, var(--primary-navy) 0%, #2d3e50 100%);
            border-radius: 8px;
            padding: 3rem;
            color: var(--white);
            margin-bottom: 3rem;
            position: relative;
            overflow: hidden;
        }

        .casestudy-hero::before {
            content: '';
            position: absolute;
            top: -60px;
            right: -60px;
            width: 220px;
            height: 220px;
            border: 3px solid rgba(255,180,0,0.2);
            border-radius: 50%;
        }

        .casestudy-hero::after {
            content: '';
            position: absolute;
            bottom: -40px;
            left: -40px;
            width: 140px;
            height: 140px;
            background: rgba(233,78,60,0.12);
            transform: rotate(45deg);
        }

        .cs-badge {
            display: inline-block;
            background: var(--accent-amber);
            color: var(--primary-navy);
            padding: 0.4rem 1.2rem;
            font-weight: 700;
            font-size: 0.75rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            border-radius: 2px;
            margin-bottom: 1.5rem;
        }

        .casestudy-hero h3 {
            font-size: 2rem;
            color: var(--white);
            margin-bottom: 0.5rem;
            line-height: 1.2;
        }

        .casestudy-hero h3 em {
            color: var(--accent-amber);
            font-style: italic;
        }

        .casestudy-hero p {
            color: rgba(255,255,255,0.8);
            max-width: 600px;
            font-size: 1rem;
            line-height: 1.7;
            margin-top: 0.75rem;
        }

        .cs-pills {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
            margin-top: 1.5rem;
        }

        .cs-pill {
            background: rgba(255,255,255,0.1);
            color: rgba(255,255,255,0.85);
            border: 1px solid rgba(255,255,255,0.2);
            padding: 0.35rem 1rem;
            border-radius: 2px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        .cs-metrics {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .cs-metric {
            background: var(--white);
            border-radius: 8px;
            padding: 2rem 1.5rem;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.07);
            border-top: 4px solid var(--accent-coral);
            transition: transform 0.3s;
        }

        .cs-metric:nth-child(2) { border-top-color: var(--accent-amber); }
        .cs-metric:nth-child(3) { border-top-color: var(--highlight-sage); }

        .cs-metric:hover {
            transform: translateY(-4px);
        }

        .cs-metric-num {
            font-family: 'Playfair Display', serif;
            font-size: 2.8rem;
            color: var(--primary-navy);
            display: block;
            line-height: 1;
            margin-bottom: 0.5rem;
        }

        .cs-metric-label {
            font-size: 0.85rem;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .cs-metric-platform {
            font-size: 0.75rem;
            color: var(--accent-coral);
            font-weight: 600;
            margin-top: 0.3rem;
        }

        .cs-metric:nth-child(2) .cs-metric-platform { color: var(--accent-amber); }
        .cs-metric:nth-child(3) .cs-metric-platform { color: var(--highlight-sage); }

        .cs-body {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .cs-card {
            background: var(--white);
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.07);
            border-left: 5px solid var(--accent-amber);
        }

        .cs-card:nth-child(2) { border-left-color: var(--accent-coral); }
        .cs-card:nth-child(3) { border-left-color: var(--highlight-sage); }
        .cs-card:nth-child(4) { border-left-color: var(--primary-navy); }

        .cs-card h4 {
            color: var(--primary-navy);
            font-size: 1.1rem;
            margin-bottom: 0.75rem;
        }

        .cs-card p {
            color: var(--text-light);
            font-size: 0.95rem;
            line-height: 1.7;
        }

        .cs-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .cs-tag {
            background: var(--neutral-warm);
            color: var(--text-dark);
            font-size: 0.75rem;
            padding: 0.3rem 0.8rem;
            border-radius: 2px;
            font-weight: 500;
        }

        .cs-timeline {
            background: var(--white);
            border-radius: 8px;
            padding: 2rem 2.5rem;
            box-shadow: 0 4px 15px rgba(0,0,0,0.07);
            margin-bottom: 2rem;
        }

        .cs-timeline h4 {
            color: var(--primary-navy);
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid var(--neutral-warm);
        }

        .cs-tl-item {
            display: flex;
            gap: 1.5rem;
            padding-bottom: 1.5rem;
            position: relative;
        }

        .cs-tl-item:not(:last-child)::after {
            content: '';
            position: absolute;
            left: 19px;
            top: 40px;
            bottom: 0;
            width: 2px;
            background: var(--accent-amber);
            opacity: 0.3;
        }

        .cs-tl-dot {
            width: 40px;
            height: 40px;
            background: var(--primary-navy);
            color: var(--accent-amber);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Playfair Display', serif;
            font-weight: 700;
            font-size: 1rem;
            flex-shrink: 0;
        }

        .cs-tl-content { flex: 1; }

        .cs-tl-title {
            font-weight: 600;
            color: var(--primary-navy);
            font-size: 0.95rem;
            margin-bottom: 0.25rem;
        }

        .cs-tl-date {
            font-size: 0.8rem;
            color: var(--accent-coral);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 0.4rem;
        }

        .cs-tl-body {
            font-size: 0.9rem;
            color: var(--text-light);
            line-height: 1.6;
        }

        .cs-takeaway {
            background: var(--primary-navy);
            color: var(--white);
            border-radius: 8px;
            padding: 2.5rem;
            border-left: 5px solid var(--accent-amber);
        }

        .cs-takeaway h4 {
            color: var(--accent-amber);
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }

        .cs-takeaway p {
            color: rgba(255,255,255,0.85);
            font-size: 1rem;
            line-height: 1.8;
            font-style: italic;
        }

        .cs-bar-wrap {
            margin-top: 1.5rem;
        }

        .cs-bar-row {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 0.9rem;
        }

        .cs-bar-label {
            font-size: 0.85rem;
            color: rgba(255,255,255,0.7);
            width: 120px;
            flex-shrink: 0;
        }

        .cs-bar-track {
            flex: 1;
            height: 6px;
            background: rgba(255,255,255,0.15);
            border-radius: 99px;
            overflow: hidden;
        }

        .cs-bar-fill {
            height: 100%;
            border-radius: 99px;
            background: var(--accent-amber);
        }

        .cs-bar-val {
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--accent-amber);
            width: 50px;
            text-align: right;
            flex-shrink: 0;
        }

        @media (max-width: 768px) {
            .cs-metrics { grid-template-columns: 1fr; }
            .cs-body { grid-template-columns: 1fr; }
        }

        /* Process Section */
        .process-section {
            background: var(--primary-navy);
            color: var(--white);
        }

        .process-section .section-header h2 {
            color: var(--white);
        }

        .process-section .section-header p {
            color: rgba(255, 255, 255, 0.7);
        }

        .process-grid {
            display: grid;
            grid-template-columns: repeat(6, 1fr);
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .process-step {
            text-align: center;
            position: relative;
        }

        .process-step::after {
            content: '→';
            position: absolute;
            right: -1rem;
            top: 2rem;
            color: var(--accent-amber);
            font-size: 1.5rem;
        }

        .process-step:last-child::after {
            display: none;
        }

        .step-number {
            width: 60px;
            height: 60px;
            background: var(--accent-coral);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 700;
            margin: 0 auto 1rem;
            font-family: 'Playfair Display', serif;
        }

        .process-step h4 {
            color: var(--accent-amber);
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
        }

        .process-step p {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.8);
        }

        /* Achievements Section */
        .achievements-section {
            background: var(--neutral-warm);
        }

        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 3rem;
            align-items: center;
        }

        .achievement-cards {
            display: grid;
            gap: 1.5rem;
        }

        .achievement-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
            border-left: 5px solid var(--accent-coral);
            transition: transform 0.3s;
        }

        .achievement-card:hover {
            transform: scale(1.02);
        }

        .achievement-card h3 {
            color: var(--primary-navy);
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        .achievement-card h3 span {
            color: var(--accent-coral);
        }

        .achievement-card p {
            color: var(--text-light);
            font-size: 1rem;
        }

        .achievement-visual {
            text-align: center;
        }

        .achievement-visual img {
            max-width: 100%;
            border-radius: 8px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
        }

        /* Tools Section */
        .tools-section {
            background: var(--white);
        }

        .tools-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }

        .tool-item {
            background: var(--neutral-warm);
            padding: 2rem;
            text-align: center;
            border-radius: 8px;
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .tool-item:hover {
            border-color: var(--accent-amber);
            transform: translateY(-3px);
        }

        .tool-icon {
            width: 70px;
            height: 70px;
            background: var(--primary-navy);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1rem;
            color: var(--white);
            font-size: 1.8rem;
            font-weight: 700;
        }

        .tool-item:nth-child(2) .tool-icon { background: var(--accent-coral); }
        .tool-item:nth-child(3) .tool-icon { background: var(--highlight-sage); }
        .tool-item:nth-child(4) .tool-icon { background: var(--accent-amber); color: var(--primary-navy); }
        .tool-item:nth-child(5) .tool-icon { background: #4285F4; }
        .tool-item:nth-child(6) .tool-icon { background: #9C27B0; }
        .tool-item:nth-child(7) .tool-icon { background: #FF6B35; }
        .tool-item:nth-child(8) .tool-icon { background: var(--primary-navy); }

        .tool-item h4 {
            color: var(--primary-navy);
            margin-bottom: 0.5rem;
        }

        .tool-item p {
            font-size: 0.9rem;
            color: var(--text-light);
        }

        /* Industry Section */
        .industry-section {
            background: linear-gradient(135deg, var(--primary-navy) 0%, #2d3e50 100%);
            color: var(--white);
        }

        .industry-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .industry-text h3 {
            color: var(--accent-amber);
            font-size: 2rem;
            margin-bottom: 1.5rem;
        }

        .industry-text p {
            margin-bottom: 1.5rem;
            line-height: 1.8;
            color: rgba(255, 255, 255, 0.9);
        }

        .industry-highlights {
            list-style: none;
            margin-top: 2rem;
        }

        .industry-highlights li {
            padding: 1rem 0;
            padding-left: 2rem;
            position: relative;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .industry-highlights li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--highlight-sage);
            font-weight: bold;
            font-size: 1.2rem;
        }

        .industry-image img {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        /* Contact Section */
        .contact-section {
            background: var(--accent-coral);
            color: var(--white);
            text-align: center;
            padding: 4rem 10%;
        }

        .contact-section h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .contact-section p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            background: var(--white);
            color: var(--accent-coral);
            padding: 1rem 3rem;
            text-decoration: none;
            font-weight: 700;
            border-radius: 4px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        /* Footer */
        footer {
            background: var(--primary-navy);
            color: rgba(255, 255, 255, 0.6);
            text-align: center;
            padding: 2rem;
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .process-grid {
                grid-template-columns: repeat(3, 1fr);
            }
            .process-step:nth-child(3)::after {
                display: none;
            }
            .tools-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .cover-content h1 {
                font-size: 2.5rem;
            }
            .cover-stats {
                flex-direction: column;
                gap: 2rem;
            }
            .summary-grid,
            .achievements-grid,
            .industry-content {
                grid-template-columns: 1fr;
            }
            .skills-container {
                grid-template-columns: 1fr;
            }
            .process-grid {
                grid-template-columns: 1fr;
            }
            .process-step::after {
                display: none;
            }
            .tools-grid {
                grid-template-columns: 1fr;
            }
            nav ul {
                flex-wrap: wrap;
                gap: 1rem;
            }
            section {
                padding: 3rem 5%;
            }
        }

        /* Print Styles */
        @media print {
            nav {
                display: none;
            }
            .cover-section {
                min-height: auto;
                padding: 3rem;
            }
            section {
                padding: 2rem;
                page-break-inside: avoid;
            }
        }
    </style>
</head>
<body>

    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#cover">Home</a></li>
            <li><a href="#summary">Profile</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#casestudy">Case Study</a></li>
            <li><a href="#process">Process</a></li>
            <li><a href="#achievements">Impact</a></li>
            <li><a href="#tools">Tools</a></li>
            <li><a href="#industry">Industry</a></li>
        </ul>
    </nav>
    <!-- Cover Section -->
    <section id="cover" class="cover-section">
        <div class="geometric-shapes">
            <div class="shape shape-1"></div>
            <div class="shape shape-2"></div>
            <div class="shape shape-3"></div>
        </div>
        <div class="cover-content">

            <h1>Deborah Nyanchama</h1>
            <p class="title">Digital Marketing Specialist</p>
            <p class="cover-tagline">Driving measurable growth through strategic prospecting, client acquisition, and digital advertising solutions. Transforming leads into lasting partnerships.</p>
            <div class="cover-stats">
                <div class="stat-item">
                    <span class="stat-number">3+</span>
                    <span class="stat-label">Years Experience</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number">200+</span>
                    <span class="stat-label">Retail Accounts</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number">28%</span>
                    <span class="stat-label">Repeat Business Growth</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Professional Summary -->
    <section id="summary" class="summary-section">
        <div class="section-header">
            <h2>Professional Summary</h2>
            <p>An overview of career achievements and value proposition</p>
        </div>
        <div class="summary-grid">
            <div class="summary-text">
                <p>Results-driven <strong>B2B/B2C Sales Executive</strong> with 3 years of progressive experience in lead generation, client acquisition, and account management within the advertising industry. Proven track record of prospecting, negotiating, and closing high-value deals while maintaining exceptional client relationships.</p>
                
                <p>Specialized in <strong>digital advertising solutions</strong>, I excel at translating complex marketing concepts into compelling value propositions that drive client success. My approach combines data-driven insights with personalized relationship building to deliver measurable ROI.</p>
                
                <div class="highlight-box">
                    <p>"I don't just sell advertising space—I deliver growth engines that transform businesses and create lasting market impact."</p>
                </div>
                
                <p>Expert in leveraging CRM tools, digital marketing analytics, and market research to identify opportunities, optimize pipelines, and exceed sales targets consistently. Passionate about connecting brands with their ideal audiences through strategic advertising placement.</p>
            </div>
            <div class="summary-image">
                <img src="Ad solutions.png" alt="Sales Executive Presenting Advertising Solutions">
            </div>
        </div>
    </section>

    <!-- Core Skills -->
    <section id="skills" class="skills-section">
        <div class="section-header">
            <h2>Core Skills & Abilities</h2>
            <p>Comprehensive expertise across sales, technology, and relationship management</p>
        </div>
        <div class="skills-container">
            <div class="skill-card">
                <div class="skill-icon">💼</div>
                <h3>Hard Skills</h3>
                <ul class="skill-list">
                    <li>Digital Advertising Solutions</li>
                    <li>Print Media Sales</li>
                    <li>Account Management</li>
                    <li>CRM Systems & Pipeline Management</li>
                    <li>Market Research & Analysis</li>
                    <li>Sales Forecasting & Reporting</li>
                    <li>B2B Lead Generation</li>
                </ul>
            </div>
            <div class="skill-card">
                <div class="skill-icon">🤝</div>
                <h3>Soft Skills</h3>
                <ul class="skill-list">
                    <li>Strategic Negotiation</li>
                    <li>Executive Presentation</li>
                    <li>Customer Relationship Management</li>
                    <li>Consultative Selling</li>
                    <li>Cross-functional Collaboration</li>
                    <li>Problem Solving</li>
                    <li>Time Management</li>
                </ul>
            </div>
            <div class="skill-card">
                <div class="skill-icon">⚡</div>
                <h3>Technical Skills</h3>
                <ul class="skill-list">
                    <li>Meta Business Suite</li>
                    <li>Google Analytics</li>
                    <li>SEO/SEM Strategies</li>
                    <li>Zapier Automation</li>
                    <li>Statista Research</li>
                    <li>AI Tools (Manus, Claude)</li>
                    <li>Data Visualization</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Experience -->
    <section id="experience" class="experience-section">
        <div class="section-header">
            <h2>Professional Experience</h2>
            <p>Track record of securing partnerships and driving revenue growth</p>
        </div>
        <div class="exp-container">
            <div class="exp-item">
                <div class="exp-timeline">
                    <div class="exp-dot"></div>
                </div>
                <div class="exp-content">
                    <span class="role">B2B Sales Executive | Advertising Sector</span>
                    <h3>Strategic Account Development</h3>
                    <p>Leading B2B sales initiatives focused on digital and print advertising solutions for diverse client portfolio.</p>
                    <ul class="exp-achievements">
                        <li><strong>Client Acquisition:</strong> Prospected and secured partnerships with 50+ new B2B clients across retail, hospitality, and professional services sectors</li>
                        <li><strong>Revenue Growth:</strong> Consistently exceeded quarterly sales targets by average of 115% through strategic upselling and cross-selling initiatives</li>
                        <li><strong>Account Expansion:</strong> Increased average contract value by 35% through consultative needs analysis and tailored solution presentation</li>
                        <li><strong>Pipeline Management:</strong> Maintained active pipeline of 150+ qualified opportunities using CRM-driven forecasting and prioritization</li>
                    </ul>
                </div>
            </div>
            <div class="exp-item">
                <div class="exp-timeline">
                    <div class="exp-dot"></div>
                </div>
                <div class="exp-content">
                    <span class="role">Digital Advertising Specialist</span>
                    <h3>Integrated Media Solutions</h3>
                    <p>Specialized in creating comprehensive advertising campaigns combining traditional print and cutting-edge digital channels.</p>
                    <ul class="exp-achievements">
                        <li><strong>Solution Architecture:</strong> Designed integrated marketing campaigns leveraging both print circulation (200K+ reach) and digital platforms</li>
                        <li><strong>ROI Optimization:</strong> Implemented tracking mechanisms that demonstrated 3:1 average return on ad spend for clients</li>
                        <li><strong>Product Innovation:</strong> Launched new digital advertising packages resulting in 40% increase in digital revenue stream</li>
                        <li><strong>Client Retention:</strong> Achieved 92% client retention rate through proactive account management and performance reviews</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Case Study Section -->
    <section id="casestudy" class="casestudy-section">
        <div class="section-header">
            <h2>Case Study</h2>
            <p>A deep-dive into a real campaign — strategy, execution, and results</p>
        </div>

        <!-- Hero card -->
        <div class="casestudy-hero">
            <div class="cs-badge">Case Study · 2023–2026</div>
            <h3>From 0 to 135K —<br><em>Growing a Kenyan Retail Brand</em> Through Social Media</h3>
            <p>How I built Onestopshop F3's digital presence from scratch, scaling Instagram and TikTok into the brand's most powerful sales channels in Kenya's beauty and lifestyle market.</p>
            <div class="cs-pills">
                <span class="cs-pill">Digital Strategy</span>
                <span class="cs-pill">Content Marketing</span>
                <span class="cs-pill">Paid Advertising</span>
                <span class="cs-pill">Instagram</span>
                <span class="cs-pill">TikTok</span>
                <span class="cs-pill">Influencer Partnerships</span>
                <span class="cs-pill">Brand Positioning</span>
            </div>
        </div>

        <!-- Metrics -->
        <div class="cs-metrics">
            <div class="cs-metric">
                <span class="cs-metric-num">135K+</span>
                <div class="cs-metric-label">Followers Gained</div>
                <div class="cs-metric-platform">Instagram</div>
            </div>
            <div class="cs-metric">
                <span class="cs-metric-num">30K+</span>
                <div class="cs-metric-label">Followers Gained</div>
                <div class="cs-metric-platform">TikTok</div>
            </div>
            <div class="cs-metric">
                <span class="cs-metric-num">177K+</span>
                <div class="cs-metric-label">Total Likes</div>
                <div class="cs-metric-platform">TikTok Engagement</div>
            </div>
        </div>

        <!-- Challenge -->
        <div class="cs-timeline" style="margin-bottom: 2rem;">
            <h4>The Challenge</h4>
            <p style="color: var(--text-light); font-size: 0.95rem; line-height: 1.8;">Onestopshop F3 had a strong physical retail presence selling fragrance, skincare, and fashion accessories — but virtually no digital footprint. The goal was to build an online brand identity from the ground up, attract a loyal following in Kenya's competitive beauty and lifestyle space, and convert that audience into paying customers.</p>
            <div class="highlight-box" style="margin-top: 1.5rem; margin-bottom: 0;">
                <p>"We needed to show that affordable could still feel aspirational — and that Kenyan shoppers deserved a brand that spoke their language."</p>
            </div>
        </div>

        <!-- Strategy cards -->
        <div class="cs-body">
            <div class="cs-card">
                <h4>Content Strategy</h4>
                <p>Built a consistent content calendar around trending audio, product showcases, and culturally relevant moments. Leaned into TikTok's discovery algorithm with original sounds and duet/stitch mechanics to maximise organic reach.</p>
                <div class="cs-tags">
                    <span class="cs-tag">#affordablebagskenya</span>
                    <span class="cs-tag">#corporatebags</span>
                    <span class="cs-tag">Original Sounds</span>
                    <span class="cs-tag">Trending Hashtags</span>
                </div>
            </div>
            <div class="cs-card">
                <h4>Influencer Partnerships</h4>
                <p>Identified and collaborated with mid-tier Kenyan lifestyle creators to extend reach authentically. Focused on creators whose audiences overlapped with the brand's target demographic in beauty and fashion.</p>
                <div class="cs-tags">
                    <span class="cs-tag">Gifting Campaigns</span>
                    <span class="cs-tag">Co-created Content</span>
                    <span class="cs-tag">Reviews & Unboxing</span>
                </div>
            </div>
            <div class="cs-card">
                <h4>Paid Advertising</h4>
                <p>Managed targeted Meta and TikTok ad campaigns with continuous A/B testing on creatives. Used analytics to identify top-performing content and allocate budget toward proven formats to drive retail conversions.</p>
                <div class="cs-tags">
                    <span class="cs-tag">Meta Ads</span>
                    <span class="cs-tag">TikTok Ads</span>
                    <span class="cs-tag">A/B Testing</span>
                    <span class="cs-tag">ROI Tracking</span>
                </div>
            </div>
            <div class="cs-card">
                <h4>Community Engagement</h4>
                <p>Hosted TikTok Lives for product launches and flash sales. Ran giveaways and Instagram Stories polls to keep the audience interactive and invested in the brand's journey, boosting loyalty and repeat purchases.</p>
                <div class="cs-tags">
                    <span class="cs-tag">TikTok Lives</span>
                    <span class="cs-tag">Giveaways</span>
                    <span class="cs-tag">IG Stories</span>
                    <span class="cs-tag">Flash Sales</span>
                </div>
            </div>
        </div>

        <!-- Timeline -->
        <div class="cs-timeline">
            <h4>Campaign Timeline</h4>
            <div class="cs-tl-item">
                <div class="cs-tl-dot">01</div>
                <div class="cs-tl-content">
                    <div class="cs-tl-date">Jan – Apr 2023</div>
                    <div class="cs-tl-title">Foundation & Brand Voice</div>
                    <div class="cs-tl-body">Established visual identity, content pillars, and posting cadence. Built initial audience through organic reach and a targeted hashtag strategy tailored to Kenyan retail shoppers.</div>
                </div>
            </div>
            <div class="cs-tl-item">
                <div class="cs-tl-dot">02</div>
                <div class="cs-tl-content">
                    <div class="cs-tl-date">May 2023 – Mid 2024</div>
                    <div class="cs-tl-title">Growth Acceleration</div>
                    <div class="cs-tl-body">Launched influencer collaborations and scaled TikTok content output. First paid campaigns deployed with retargeting funnels to drive measurable store traffic and online enquiries.</div>
                </div>
            </div>
            <div class="cs-tl-item">
                <div class="cs-tl-dot">03</div>
                <div class="cs-tl-content">
                    <div class="cs-tl-date">Late 2024 – Jan 2026</div>
                    <div class="cs-tl-title">Community & Conversion Focus</div>
                    <div class="cs-tl-body">Scaled TikTok Lives and giveaway campaigns. Optimised ad spend based on performance data, significantly boosting ROI and repeat purchase rates among existing customers.</div>
                </div>
            </div>
        </div>

        <!-- Takeaway with bar chart -->
        <div class="cs-takeaway">
            <h4>Key Results & Takeaway</h4>
            <div class="cs-bar-wrap">
                <div class="cs-bar-row">
                    <span class="cs-bar-label">Instagram</span>
                    <div class="cs-bar-track"><div class="cs-bar-fill" style="width:92%"></div></div>
                    <span class="cs-bar-val">135K</span>
                </div>
                <div class="cs-bar-row">
                    <span class="cs-bar-label">TikTok Followers</span>
                    <div class="cs-bar-track"><div class="cs-bar-fill" style="width:22%; background: var(--accent-coral);"></div></div>
                    <span class="cs-bar-val" style="color:var(--accent-coral);">30K</span>
                </div>
                <div class="cs-bar-row">
                    <span class="cs-bar-label">TikTok Likes</span>
                    <div class="cs-bar-track"><div class="cs-bar-fill" style="width:100%; background: var(--highlight-sage);"></div></div>
                    <span class="cs-bar-val" style="color:var(--highlight-sage);">177K</span>
                </div>
            </div>
            <p style="margin-top: 1.5rem;">This project proved that a retail brand in an emerging market can compete and win on social media through consistent, authentic content — without a massive budget. The key was understanding the audience deeply, moving fast on trends, and treating every follower as a potential loyal customer rather than just a number.</p>
        </div>
    </section>

    <!-- Process of Work -->
    <section id="process" class="process-section">
        <div class="section-header">
            <h2>Process of Work</h2>
            <p>A systematic approach to converting prospects into loyal clients</p>
        </div>
        <div class="process-grid">
            <div class="process-step">
                <div class="step-number">1</div>
                <h4>Prospecting</h4>
                <p>Market research and lead identification using data-driven targeting criteria</p>
            </div>
            <div class="process-step">
                <div class="step-number">2</div>
                <h4>Engagement</h4>
                <p>Strategic outreach via multi-channel approach with personalized messaging</p>
            </div>
            <div class="process-step">
                <div class="step-number">3</div>
                <h4>Discovery</h4>
                <p>In-depth needs analysis to understand client objectives and pain points</p>
            </div>
            <div class="process-step">
                <div class="step-number">4</div>
                <h4>Solution</h4>
                <p>Customized advertising proposals with clear ROI projections</p>
            </div>
            <div class="process-step">
                <div class="step-number">5</div>
                <h4>Closing</h4>
                <p>Strategic negotiation and seamless contract execution</p>
            </div>
            <div class="process-step">
                <div class="step-number">6</div>
                <h4>Retention</h4>
                <p>Ongoing relationship management and performance optimization</p>
            </div>
        </div>
    </section>

    <!-- Achievements -->
    <section id="achievements" class="achievements-section">
        <div class="section-header">
            <h2>Achievements & Impact</h2>
            <p>Quantifiable results that demonstrate consistent excellence</p>
        </div>
        <div class="achievements-grid">
            <div class="achievement-cards">
                <div class="achievement-card">
                    <h3><span>28%</span> Increase</h3>
                    <p>Boosted repeat business among 200+ retail accounts through strategic account management and proactive engagement initiatives</p>
                </div>
                <div class="achievement-card">
                    <h3><span>35%</span> Growth</h3>
                    <p>Expanded product offerings per client by identifying cross-sell opportunities and demonstrating integrated solution value</p>
                </div>
                <div class="achievement-card">
                    <h3><span>115%</span> Target</h3>
                    <p>Average quarterly sales target achievement through disciplined pipeline management and consultative selling approach</p>
                </div>
                <div class="achievement-card">
                    <h3><span>92%</span> Retention</h3>
                    <p>Client retention rate maintained through exceptional post-sale support and continuous value delivery</p>
                </div>
            </div>
            <div class="achievement-visual">
                <img src="Growth&sales.png" alt="Business Growth and Sales Success">
            </div>
        </div>
    </section>

    <!-- Tools -->
    <section id="tools" class="tools-section">
        <div class="section-header">
            <h2>Technology Stack</h2>
            <p>Advanced tools that power sales excellence and client insights</p>
        </div>
        <div class="tools-grid">
            <div class="tool-item">
                <div class="tool-icon">M</div>
                <h4>Meta Business Suite</h4>
                <p>Social media advertising management and campaign optimization</p>
            </div>
            <div class="tool-item">
                <div class="tool-icon">G</div>
                <h4>Google Analytics</h4>
                <p>Web traffic analysis and conversion tracking</p>
            </div>
            <div class="tool-item">
                <div class="tool-icon">S</div>
                <h4>SEO/SEM</h4>
                <p>Search engine optimization and paid search management</p>
            </div>
            <div class="tool-item">
                <div class="tool-icon">Z</div>
                <h4>Zapier</h4>
                <p>Workflow automation and CRM integration</p>
            </div>
            <div class="tool-item">
                <div class="tool-icon">St</div>
                <h4>Statista</h4>
                <p>Market research and industry data analysis</p>
            </div>
            <div class="tool-item">
                <div class="tool-icon">Ma</div>
                <h4>Manus</h4>
                <p>AI-powered research and automation</p>
            </div>
            <div class="tool-item">
                <div class="tool-icon">Cl</div>
                <h4>Claude</h4>
                <p>AI assistant for content and strategy</p>
            </div>
            <div class="tool-item">
                <div class="tool-icon">CRM</div>
                <h4>CRM Systems</h4>
                <p>Pipeline management and client tracking</p>
            </div>
        </div>
        
        <div style="margin-top: 4rem; display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; align-items: center;">
            <div>
                <img src="https://kimi-web-img.moonshot.cn/img/siliconvalley.center/66939effb2988a42685f33d45f68a48eeab6e396.jpg" alt="Digital vs Print Advertising Comparison" style="width: 100%; border-radius: 8px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
            </div>
            <div>
                <img src="CRM mgt.png" alt="CRM and Client Management" style="width: 100%; border-radius: 8px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
            </div>
        </div>
    </section>

    <!-- Industry Exposure -->
    <section id="industry" class="industry-section">
        <div class="section-header">
            <h2 style="color: white;">Industry Exposure</h2>
            <p style="color: rgba(255,255,255,0.7);">Global networking and cross-industry insights</p>
        </div>
        <div class="industry-content">
            <div class="industry-text">
                <h3>Beauty World Expo 2025</h3>
                <p>Participated in one of the industry's premier international exhibitions, gaining invaluable exposure to global market trends and emerging consumer behaviors.</p>
                <p>This experience expanded my understanding of cross-industry advertising needs and reinforced the importance of culturally-aware marketing strategies in today's globalized marketplace.</p>
                
                <ul class="industry-highlights">
                    <li>Networked with 100+ international suppliers and potential clients from 30+ countries</li>
                    <li>Gained insights into beauty industry advertising trends and digital transformation</li>
                    <li>Established connections with key decision-makers in retail and distribution</li>
                    <li>Observed emerging marketing technologies and their application in B2B/B2C contexts</li>
                    <li>Developed understanding of cross-cultural business communication nuances</li>
                </ul>
            </div>
            <div class="industry-image ">
                <img src="Digital & Industry trends.png" alt="Digital and Industry Trends">
            </div>
            <div class="industry-image">
                <img src="Digital Industry woman.png" alt="Digital and Industry Trends 2">
            </div>    
        </div>
    </section>

    <!-- Contact CTA -->
    <section class="contact-section">
        <h2>Ready to Drive Growth Together?</h2>
        <p>Let's discuss how strategic advertising solutions can transform your business outcomes</p>
        <a href="mailto:deborahnyanchama744@gmail.com" class="cta-button">Get In Touch</a>
        <p>deborahnyanchama744@gmail.com</p>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Deborah Nyanchama. Professional Portfolio. All rights reserved.</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all cards and sections
        document.querySelectorAll('.skill-card, .achievement-card, .exp-item, .tool-item, .cs-metric, .cs-card, .cs-tl-item').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });
    </script>

</body>
</html>
