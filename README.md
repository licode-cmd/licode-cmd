<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>LICODE — Crafting Digital Experiences</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: radial-gradient(ellipse at 50% 0%, #1a1410 0%, #0c0a08 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            padding: 60px 24px;
            font-family: 'Inter', sans-serif;
            color: #e8ddd0;
            line-height: 1.6;
        }

        .container {
            max-width: 960px;
            width: 100%;
        }

        /* --- GOLD ACCENT --- */
        .gold {
            color: #c9a96e;
        }

        .gold-border {
            border-color: #c9a96e;
        }

        /* --- HEADER --- */
        .hero {
            text-align: center;
            padding: 40px 0 30px;
            border-bottom: 1px solid rgba(201, 169, 110, 0.2);
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 4rem;
            font-weight: 600;
            letter-spacing: 8px;
            color: #c9a96e;
            text-shadow: 0 0 60px rgba(201, 169, 110, 0.1);
        }

        .hero .sub {
            font-size: 1.1rem;
            letter-spacing: 6px;
            font-weight: 300;
            color: #d4cdc0;
            margin-top: 8px;
        }

        .hero .tagline {
            font-size: 1.05rem;
            color: #a89f92;
            margin-top: 20px;
            font-weight: 300;
        }

        .hero .tagline span {
            color: #c9a96e;
            font-weight: 400;
        }

        .hero .divider {
            width: 80px;
            height: 1px;
            background: #c9a96e;
            margin: 24px auto 18px;
            opacity: 0.5;
        }

        .hero .pillars {
            font-size: 0.8rem;
            letter-spacing: 5px;
            color: #a89f92;
            font-weight: 300;
        }

        /* --- SECTION --- */
        section {
            margin-top: 56px;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.6rem;
            font-weight: 400;
            letter-spacing: 3px;
            color: #c9a96e;
            margin-bottom: 18px;
            border-bottom: 1px solid rgba(201, 169, 110, 0.15);
            padding-bottom: 10px;
        }

        .section-title.light {
            color: #e8ddd0;
            border-bottom-color: rgba(255, 255, 255, 0.06);
        }

        .text-muted {
            color: #a89f92;
            font-weight: 300;
        }

        /* --- ABOUT --- */
        .about p {
            font-size: 1rem;
            color: #cfc6b8;
            margin-bottom: 6px;
        }

        .about .highlight {
            color: #f0e8dc;
            font-weight: 500;
        }

        .about .italic {
            font-family: 'Playfair Display', serif;
            font-style: italic;
            font-size: 1.1rem;
            color: #c9a96e;
            margin-top: 10px;
        }

        /* --- GRID PROVIDE --- */
        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 8px;
        }

        .card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(4px);
            border: 1px solid rgba(201, 169, 110, 0.12);
            border-radius: 16px;
            padding: 24px 22px;
            transition: all 0.3s ease;
        }

        .card:hover {
            background: rgba(201, 169, 110, 0.06);
            border-color: rgba(201, 169, 110, 0.35);
            transform: translateY(-4px);
            box-shadow: 0 20px 40px -20px rgba(0, 0, 0, 0.7);
        }

        .card h3 {
            font-family: 'Playfair Display', serif;
            font-weight: 400;
            font-size: 1.2rem;
            letter-spacing: 1px;
            color: #f0e8dc;
            margin-bottom: 8px;
        }

        .card p {
            font-size: 0.92rem;
            color: #b0a69a;
            font-weight: 300;
            line-height: 1.7;
        }

        /* --- TECH STACK --- */
        .tech-wrap {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 4px;
        }

        .tech-badge {
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(201, 169, 110, 0.15);
            padding: 8px 20px;
            border-radius: 40px;
            font-size: 0.8rem;
            letter-spacing: 1.5px;
            color: #d4cdc0;
            font-weight: 300;
            transition: 0.3s;
        }

        .tech-badge:hover {
            background: rgba(201, 169, 110, 0.1);
            border-color: #c9a96e;
            color: #f0e8dc;
        }

        /* --- PHILOSOPHY --- */
        blockquote {
            font-family: 'Playfair Display', serif;
            font-size: 1.6rem;
            font-weight: 400;
            font-style: italic;
            color: #f0e8dc;
            border-left: 3px solid #c9a96e;
            padding-left: 24px;
            margin: 8px 0 16px;
        }

        .philosophy p {
            color: #b0a69a;
            font-weight: 300;
            margin-bottom: 4px;
        }

        .philosophy .bullets {
            margin-top: 14px;
        }

        .philosophy .bullets span {
            display: block;
            color: #cfc6b8;
            font-weight: 300;
        }

        .philosophy .bullets .dot {
            color: #c9a96e;
            margin-right: 8px;
        }

        /* --- SOCIAL --- */
        .social-wrap {
            display: flex;
            flex-wrap: wrap;
            gap: 14px;
            margin-top: 6px;
        }

        .social-link {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(201, 169, 110, 0.12);
            padding: 8px 24px;
            border-radius: 40px;
            font-size: 0.75rem;
            letter-spacing: 2px;
            color: #b0a69a;
            text-decoration: none;
            transition: 0.3s;
            font-weight: 300;
        }

        .social-link:hover {
            background: rgba(201, 169, 110, 0.1);
            border-color: #c9a96e;
            color: #f0e8dc;
        }

        /* --- COLLAB --- */
        .collab p {
            color: #b0a69a;
            font-weight: 300;
        }

        .collab .big {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            letter-spacing: 6px;
            color: #c9a96e;
            margin-top: 14px;
        }

        .collab .role {
            font-size: 0.8rem;
            letter-spacing: 2px;
            color: #7a7268;
        }

        /* --- FOOTER --- */
        .footer {
            text-align: center;
            margin-top: 56px;
            padding-top: 28px;
            border-top: 1px solid rgba(201, 169, 110, 0.12);
        }

        .footer h4 {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            letter-spacing: 4px;
            color: #c9a96e;
            font-weight: 400;
        }

        .footer p {
            color: #7a7268;
            font-style: italic;
            font-size: 0.9rem;
            margin-top: 2px;
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 640px) {
            .hero h1 {
                font-size: 2.6rem;
                letter-spacing: 4px;
            }
            .grid-2 {
                grid-template-columns: 1fr;
            }
            .section-title {
                font-size: 1.3rem;
            }
            blockquote {
                font-size: 1.2rem;
                padding-left: 16px;
            }
        }
    </style>
</head>
<body>

    <div class="container">

        <!-- HERO -->
        <div class="hero">
            <h1>LICODE</h1>
            <div class="sub">CRAFTING DIGITAL EXPERIENCES</div>
            <div class="tagline">
                A creative front-end space built with precision —<br />
                <span>modern interfaces, interactive components, and premium web templates.</span>
            </div>
            <div class="divider"></div>
            <div class="pillars">BUILD · DESIGN · EXPERIMENT · SHARE</div>
        </div>

        <!-- ABOUT -->
        <section class="about">
            <div class="section-title">ABOUT LICODE</div>
            <p><span class="highlight">LICODE</span> is a front-end development space dedicated to crafting clean, modern, and immersive web experiences.</p>
            <p>From small UI components to complete web templates, every project is built with a focus on <span class="gold">visual quality, usability,</span> and <span style="color:#f0e8dc;">flawless implementation.</span></p>
            <div class="italic">LICODE is where ideas become interfaces.</div>
        </section>

        <!-- PROVIDE -->
        <section>
            <div class="section-title">WHAT WE PROVIDE</div>
            <div class="grid-2">
                <div class="card">
                    <h3>FREE TEMPLATES</h3>
                    <p>Accessible front-end templates and components created for learning, experimentation, and personal projects.</p>
                </div>
                <div class="card">
                    <h3>PREMIUM TEMPLATES</h3>
                    <p>Advanced and polished interfaces designed for developers who want <span class="gold">ready-to-use front-end resources.</span></p>
                </div>
                <div class="card">
                    <h3>UI COMPONENTS</h3>
                    <p>Interactive cards, buttons, navigation, animations, forms, and other reusable front-end elements.</p>
                </div>
                <div class="card">
                    <h3>CREATIVE EXPERIMENTS</h3>
                    <p>Experimental interfaces and visual concepts exploring modern web design and front-end development.</p>
                </div>
            </div>
        </section>

        <!-- TECH -->
        <section>
            <div class="section-title">TECH STACK</div>
            <div class="tech-wrap">
                <span class="tech-badge">HTML5</span>
                <span class="tech-badge">CSS3</span>
                <span class="tech-badge">JavaScript</span>
                <span class="tech-badge">Git</span>
                <span class="tech-badge">GitHub</span>
            </div>
        </section>

        <!-- PHILOSOPHY -->
        <section class="philosophy">
            <div class="section-title">THE PHILOSOPHY</div>
            <blockquote>Simple doesn't mean ordinary.</blockquote>
            <p>We believe great interfaces don't need unnecessary complexity.</p>
            <p>Every detail matters — from the structure of the code to the smallest interaction on the screen.</p>
            <div class="bullets">
                <span><span class="dot">✦</span> Clean code.</span>
                <span><span class="dot">✦</span> Strong visuals.</span>
                <span><span class="dot">✦</span> Meaningful interactions.</span>
            </div>
        </section>

        <!-- SOCIAL -->
        <section>
            <div class="section-title light">FOLLOW THE WORK</div>
            <p class="text-muted" style="margin-bottom:14px;">Discover new interfaces, experiments, and front-end creations across our social platforms.</p>
            <div class="social-wrap">
                <a href="#" class="social-link">YOUTUBE</a>
                <a href="#" class="social-link">TIKTOK</a>
                <a href="#" class="social-link">INSTAGRAM</a>
                <a href="#" class="social-link">PINTEREST</a>
            </div>
        </section>

        <!-- COLLAB -->
        <section class="collab">
            <div class="section-title light">COLLABORATE</div>
            <p>Have an idea, project, or collaboration in mind?</p>
            <p style="color:#e8ddd0;">Let's build something worth looking at.</p>
            <div class="big">LICODE</div>
            <div class="role">Front-End Development · UI Design · Creative Web</div>
        </section>

        <!-- FOOTER -->
        <div class="footer">
            <h4>LICODE</h4>
            <p>Build something beautiful.</p>
        </div>

    </div>

</body>
</html>
