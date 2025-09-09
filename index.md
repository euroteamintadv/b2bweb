<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EuroTeam B2B Services Srl | Soluzioni Business Internazionali</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #0C71C3;
            --secondary: #E09900;
            --accent: #edbb5f;
            --dark: #2c3e50;
            --light: #f8f9fa;
            --gray: #6c757d;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
            background-color: var(--light);
        }

        h1, h2, h3, h4, h5, h6 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header e navigazione */
        header {
            background-color: white;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            height: 50px;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin: 0 15px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--secondary);
            transition: var(--transition);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .header-buttons {
            display: flex;
            align-items: center;
        }

        .language-selector {
            position: relative;
            margin-right: 20px;
        }

        .language-btn {
            background: none;
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            font-weight: 500;
        }

        .language-btn img {
            width: 20px;
            margin-right: 5px;
        }

        .language-dropdown {
            position: absolute;
            top: 100%;
            right: 0;
            background: white;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border-radius: 5px;
            padding: 10px;
            display: none;
            width: 150px;
            z-index: 1000;
        }

        .language-dropdown a {
            display: flex;
            align-items: center;
            padding: 8px 10px;
            text-decoration: none;
            color: var(--dark);
            transition: var(--transition);
        }

        .language-dropdown a:hover {
            background-color: #f5f5f5;
        }

        .language-dropdown a img {
            width: 20px;
            margin-right: 10px;
        }

        .language-selector:hover .language-dropdown {
            display: block;
        }

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--dark);
        }

        /* Hero Section */
        .hero {
            padding: 150px 0 100px;
            background: linear-gradient(135deg, var(--primary) 0%, #015c91 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .hero-text {
            flex: 1;
            padding-right: 30px;
            animation: fadeInUp 1s ease;
        }

        .hero-text h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero-text p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            text-align: center;
        }

        .btn-primary {
            background-color: var(--secondary);
            color: white;
        }

        .btn-primary:hover {
            background-color: #c28500;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .btn-outline {
            border: 2px solid white;
            color: white;
        }

        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .hero-image {
            flex: 1;
            animation: fadeInRight 1s ease;
        }

        .hero-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }

        /* Features Section */
        .features {
            padding: 100px 0;
            background-color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            margin-bottom: 15px;
        }

        .section-title h2:after {
            content: '';
            position: absolute;
            width: 50%;
            height: 3px;
            background-color: var(--secondary);
            bottom: -10px;
            left: 25%;
        }

        .section-title p {
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            text-align: center;
            opacity: 0;
            transform: translateY(20px);
            position: relative;
            z-index: 1;
            overflow: hidden;
        }

        .feature-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--primary) 0%, transparent 100%);
            opacity: 0;
            transition: var(--transition);
            z-index: -1;
        }

        .feature-card.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            color: white;
        }

        .feature-card:hover:before {
            opacity: 1;
        }

        .feature-card:hover h3,
        .feature-card:hover p {
            color: white;
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            background-color: rgba(12, 113, 195, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            color: var(--primary);
            font-size: 1.8rem;
            transition: var(--transition);
        }

        .feature-card:hover .feature-icon {
            background-color: rgba(255, 255, 255, 0.2);
            color: white;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary);
            transition: var(--transition);
        }

        .feature-card p {
            transition: var(--transition);
        }

        .feature-link {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 2;
            cursor: pointer;
        }

        /* Services Section */
        .services {
            padding: 100px 0;
            background-color: #f9f9f9;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            opacity: 0;
            transform: translateY(20px);
            position: relative;
        }

        .service-card.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .service-image {
            height: 200px;
            overflow: hidden;
            position: relative;
        }

        .service-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .service-card:hover .service-image img {
            transform: scale(1.1);
        }

        .language-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: rgba(255, 255, 255, 0.9);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            color: var(--primary);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            z-index: 3;
        }

        .language-badge i {
            margin-right: 5px;
        }

        .service-content {
            padding: 25px;
            position: relative;
        }

        .service-content h3 {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 15px;
        }

        .service-content p {
            color: var(--gray);
            margin-bottom: 20px;
        }

        .service-link {
            display: inline-flex;
            align-items: center;
            color: var(--secondary);
            text-decoration: none;
            font-weight: 600;
            position: relative;
            z-index: 3;
        }

        .service-link i {
            margin-left: 5px;
            transition: var(--transition);
        }

        .service-link:hover i {
            transform: translateX(5px);
        }

        .card-link {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 2;
            cursor: pointer;
        }

        /* Dashboard Preview */
        .dashboard-preview {
            background: linear-gradient(135deg, #2c3e50 0%, #1a2530 100%);
            padding: 60px 0;
            color: white;
            margin: 40px 0;
            border-radius: 10px;
        }

        .dashboard-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .dashboard-text {
            flex: 1;
            padding-right: 40px;
        }

        .dashboard-text h2 {
            font-size: 2.2rem;
            margin-bottom: 20px;
            color: white;
        }

        .dashboard-text p {
            margin-bottom: 25px;
            opacity: 0.9;
        }

        .dashboard-features {
            list-style: none;
            margin-bottom: 25px;
        }

        .dashboard-features li {
            margin-bottom: 12px;
            display: flex;
            align-items: center;
        }

        .dashboard-features i {
            color: var(--accent);
            margin-right: 10px;
        }

        .dashboard-image {
            flex: 1;
            text-align: center;
        }

        .dashboard-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        /* Stats Section */
        .stats {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--primary) 0%, #015c91 100%);
            color: white;
            text-align: center;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
        }

        .stat-item {
            padding: 20px;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--accent);
        }

        .stat-text {
            font-size: 1.1rem;
        }

        /* Contact Section */
        .contact {
            padding: 100px 0;
            background-color: white;
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .contact-details {
            list-style: none;
        }

        .contact-details li {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
        }

        .contact-details i {
            color: var(--secondary);
            font-size: 1.2rem;
            margin-right: 15px;
            margin-top: 5px;
        }

        .contact-form {
            background-color: #f9f9f9;
            padding: 30px;
            border-radius: 10px;
        }

        .contact-form h3 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Poppins', sans-serif;
            transition: var(--transition);
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(12, 113, 195, 0.1);
        }

        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 70px 0 20px;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-col h4 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-col h4:after {
            content: '';
            position: absolute;
            width: 50px;
            height: 2px;
            background-color: var(--secondary);
            bottom: 0;
            left: 0;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: #bbb;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: white;
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: var(--transition);
        }

        .social-links a:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* AI Chat Widget */
        .chat-widget {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 1000;
        }

        .chat-button {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: var(--primary);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
        }

        .chat-button:hover {
            background-color: var(--secondary);
            transform: scale(1.1);
        }

        .chat-container {
            position: absolute;
            bottom: 70px;
            right: 0;
            width: 380px;
            height: 500px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 5px 30px rgba(0, 0, 0, 0.1);
            display: none;
            flex-direction: column;
            overflow: hidden;
        }

        .chat-header {
            background-color: var(--primary);
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .chat-header h3 {
            margin-bottom: 0;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
        }

        .chat-header h3 i {
            margin-right: 8px;
            transition: var(--transition);
        }

        .language-indicator {
            background: rgba(255, 255, 255, 0.2);
            padding: 3px 8px;
            border-radius: 15px;
            font-size: 0.7rem;
            margin-left: 10px;
        }

        .chat-close {
            background: none;
            border: none;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
        }

        .chat-messages {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
        }

        .message {
            margin-bottom: 15px;
            display: flex;
        }

        .message.bot {
            flex-direction: row;
        }

        .message.user {
            flex-direction: row-reverse;
        }

        .message-avatar {
            width: 35px;
            height: 35px;
            border-radius: 50%;
            background-color: #f0f0f0;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 10px;
            flex-shrink: 0;
        }

        .bot .message-avatar {
            background-color: var(--primary);
            color: white;
        }

        .user .message-avatar {
            background-color: var(--secondary);
            color: white;
        }

        .message-content {
            background-color: #f0f0f0;
            padding: 10px 15px;
            border-radius: 18px;
            max-width: 70%;
        }

        .bot .message-content {
            background-color: #e6f0ff;
            border-top-left-radius: 5px;
        }

        .user .message-content {
            background-color: #dcf8c6;
            border-top-right-radius: 5px;
        }

        .chat-input-container {
            display: flex;
            padding: 15px;
            border-top: 1px solid #eee;
            align-items: center;
        }

        .language-select {
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-right: 10px;
            font-size: 0.8rem;
        }

        .chat-input {
            flex: 1;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 30px;
            outline: none;
        }

        .chat-send {
            background-color: var(--primary);
            color: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            margin-left: 10px;
            cursor: pointer;
            transition: var(--transition);
        }

        .chat-send:hover {
            background-color: var(--secondary);
        }

        /* Animazioni */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInRight {
            from {
                opacity: 0;
                transform: translateX(30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
            }
            
            .hero-text {
                padding-right: 0;
                margin-bottom: 40px;
                text-align: center;
            }
            
            .hero-buttons {
                justify-content: center;
            }
            
            .dashboard-container {
                flex-direction: column;
            }
            
            .dashboard-text {
                padding-right: 0;
                margin-bottom: 30px;
                text-align: center;
            }
            
            .dashboard-features {
                text-align: left;
                max-width: 400px;
                margin: 0 auto;
            }
            
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                background-color: white;
                width: 100%;
                height: calc(100vh - 80px);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: var(--transition);
                box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .menu-toggle {
                display: block;
            }
        }

        @media (max-width: 768px) {
            .hero-text h1 {
                font-size: 2.2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .chat-container {
                width: 320px;
            }
        }

        @media (max-width: 576px) {
            .hero {
                padding: 120px 0 80px;
            }
            
            .hero-text h1 {
                font-size: 1.8rem;
            }
            
            .hero-buttons {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
                margin-bottom: 10px;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
            }
            
            .chat-container {
                width: 300px;
                right: -20px;
            }
            
            .language-select {
                display: none;
            }
        }

        /* Stili per la pagina di dettaglio */
        .service-detail-page {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: white;
            z-index: 2000;
            overflow-y: auto;
            padding: 100px 20px;
        }

        .service-detail-content {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        .service-detail-header {
            padding: 40px;
            background: linear-gradient(135deg, var(--primary) 0%, #015c91 100%);
            color: white;
            position: relative;
        }

        .service-detail-close {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.2);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: var(--transition);
        }

        .service-detail-close:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: rotate(90deg);
        }

        .service-detail-body {
            padding: 40px;
        }

        .service-detail-image {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 30px;
        }

        .service-features {
            margin: 30px 0;
        }

        .service-features li {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .service-features i {
            color: var(--secondary);
            margin-right: 10px;
        }

        .service-detail-cta {
            background-color: #f9f9f9;
            padding: 30px;
            text-align: center;
            border-radius: 10px;
            margin-top: 30px;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <img src="https://euroteamonline.ro/wp-content/uploads/2019/06/logoet.png" alt="EuroTeam B2B Services">
            </div>
            
            <button class="menu-toggle">
                <i class="fas fa-bars"></i>
            </button>
            
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Servizi</a></li>
                <li><a href="#dashboard">Dashboard</a></li>
                <li><a href="#about">Chi Siamo</a></li>
                <li><a href="#contact">Contatti</a></li>
            </ul>
            
            <div class="header-buttons">
                <div class="language-selector">
                    <button class="language-btn">
                        <img src="https://flagcdn.com/w20/it.png" alt="Italiano"> IT
                    </button>
                    <div class="language-dropdown">
                        <a href="#"><img src="https://flagcdn.com/w20/ro.png" alt="Română"> RO</a>
                        <a href="#"><img src="https://flagcdn.com/w20/gb.png" alt="English"> EN</a>
                        <a href="#"><img src="https://flagcdn.com/w20/it.png" alt="Italiano"> IT</a>
                        <a href="#"><img src="https://flagcdn.com/w20/fr.png" alt="Français"> FR</a>
                        <a href="#"><img src="https://flagcdn.com/w20/es.png" alt="Español"> ES</a>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <div class="hero-text">
                <h1>Soluzioni Business Complete per Professionisti e Aziende</h1>
                <p>EuroTeam offre servizi B2B innovativi e flessibili per supportare la crescita della tua attività in Romania e oltre.</p>
                <div class="hero-buttons">
                    <a href="#services" class="btn btn-primary">Scopri i Servizi</a>
                    <a href="#contact" class="btn btn-outline">Contattaci</a>
                </div>
            </div>
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1497366811353-6870744d04b2?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1500&q=80" alt="Team EuroTeam">
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>Perché Sceglierci</h2>
                <p>Eccellenza e affidabilità nei servizi business da oltre 22 anni</p>
            </div>
            
            <div class="features-grid">
                <div class="feature-card">
                    <a href="#feature-detail-1" class="feature-link" data-feature="1"></a>
                    <div class="feature-icon">
                        <i class="fas fa-handshake"></i>
                    </div>
                    <h3>Flessibilità</h3>
                    <p>Servizi personalizzabili in base alle esigenze specifiche di ogni cliente</p>
                </div>
                
                <div class="feature-card">
                    <a href="#feature-detail-2" class="feature-link" data-feature="2"></a>
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>Customer Care</h3>
                    <p>Assistenza dedicata multilingua con team di lunga esperienza</p>
                </div>
                
                <div class="feature-card">
                    <a href="#feature-detail-3" class="feature-link" data-feature="3"></a>
                    <div class="feature-icon">
                        <i class="fas fa-bullseye"></i>
                    </div>
                    <h3>Mission</h3>
                    <p>Migliorare la qualità della vita professionale attraverso soluzioni efficienti</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>I Nostri Servizi</h2>
                <p>Soluzioni complete per professionisti, startup e aziende consolidate</p>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <a href="#service-detail-1" class="card-link" data-service="1"></a>
                    <div class="service-image">
                        <img src="https://images.unsplash.com/photo-1560472355-536de3962603?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80" alt="Sede Legale">
                        <div class="language-badge">
                            <i class="fas fa-globe"></i> 5 lingue
                        </div>
                    </div>
                    <div class="service-content">
                        <h3>Sede Legale</h3>
                        <p>Indirizzo prestigioso a Bucarest per la registrazione della tua società con servizi amministrativi completi</p>
                        <a href="#service-detail-1" class="service-link" data-service="1">Scopri di più <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="service-card">
                    <a href="#service-detail-2" class="card-link" data-service="2"></a>
                    <div class="service-image">
                        <img src="https://images.unsplash.com/photo-1577375729152-4c8b5fcda381?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80" alt="Ufficio Virtuale">
                        <div class="language-badge">
                            <i class="fas fa-globe"></i> 5 lingue
                        </div>
                    </div>
                    <div class="service-content">
                        <h3>Ufficio Virtuale</h3>
                        <p>Servizi di segreteria, gestione corrispondenza e supporto amministrativo senza costi fissi di ufficio</p>
                        <a href="#service-detail-2" class="service-link" data-service="2">Scopri di più <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="service-card">
                    <a href="#service-detail-3" class="card-link" data-service="3"></a>
                    <div class="service-image">
                        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80" alt="E-commerce Services">
                        <div class="language-badge">
                            <i class="fas fa-globe"></i> 5 lingue
                        </div>
                    </div>
                    <div class="service-content">
                        <h3>Servizi E-commerce</h3>
                        <p>Soluzioni complete per il commercio online: consulenza, marketing digitale e gestione piattaforme</p>
                        <a href="#service-detail-3" class="service-link" data-service="3">Scopri di più <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <!-- Nuovo servizio: Assistenza Banche -->
                <div class="service-card">
                    <a href="#service-detail-4" class="card-link" data-service="4"></a>
                    <div class="service-image">
                        <img src="https://images.unsplash.com/photo-1553729459-efe14ef6055d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80" alt="Assistenza Banche">
                        <div class="language-badge">
                            <i class="fas fa-globe"></i> 5 lingue
                        </div>
                    </div>
                    <div class="service-content">
                        <h3>Assistenza Banche</h3>
                        <p>Assistenza apertura conti correnti bancari e altre operazioni complesse</p>
                        <a href="#service-detail-4" class="service-link" data-service="4">Scopri di più <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Dashboard Section -->
    <section class="dashboard-preview" id="dashboard">
        <div class="container dashboard-container">
            <div class="dashboard-text">
                <h2>Dashboard Multilingue</h2>
                <p>Monitora in tempo reale tutti i tuoi servizi attraverso la nostra piattaforma avanzata, disponibile in 5 lingue.</p>
                
                <ul class="dashboard-features">
                    <li><i class="fas fa-check-circle"></i> Supporto amministrativo in Italiano, Inglese, Rumeno, Francese e Spagnolo</li>
                    <li><i class="fas fa-check-circle"></i> Monitoraggio in tempo reale di tutte le attività</li>
                    <li><i class="fas fa-check-circle"></i> Reportistica avanzata e personalizzabile</li>
                    <li><i class="fas fa-check-circle"></i> Notifiche immediate per ogni aggiornamento</li>
                    <li><i class="fas fa-check-circle"></i> Accesso sicuro da qualsiasi dispositivo</li>
                </ul>
                
                <a href="#" class="btn btn-primary">Accedi alla Dashboard</a>
            </div>
            
            <div class="dashboard-image">
                <img src="https://images.unsplash.com/photo-1581291518633-83b4ebd1d83e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=800&q=80" alt="Dashboard EuroTeam">
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item">
                    <div class="stat-number" data-count="65">0</div>
                    <div class="stat-text">Clienti da oltre 10 anni</div>
                </div>
                
                <div class="stat-item">
                    <div class="stat-number" data-count="36">0</div>
                    <div class="stat-text">Giovani imprenditori</div>
                </div>
                
                <div class="stat-item">
                    <div class="stat-number" data-count="15">0</div>
                    <div class="stat-text">Anni di esperienza</div>
                </div>
                
                <div class="stat-item">
                    <div class="stat-number" data-count="500">0</div>
                    <div class="stat-text">Clienti soddisfatti</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contattaci</h2>
                <p>Siamo a tua disposizione per qualsiasi informazione o preventivo</p>
            </div>
            
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Informazioni di Contatto</h3>
                    <ul class="contact-details">
                        <li>
                            <i class="fas fa-map-marker-alt"></i>
                            <div>Union International Center<br>11, Ion Campineanu street<br>4th floor, Sector 1, Bucharest</div>
                        </li>
                        <li>
                            <i class="fas fa-phone"></i>
                            <div>+40 21 312 50 82</div>
                        </li>
                        <li>
                            <i class="fas fa-envelope"></i>
                            <div>office@euroteamonline.ro</div>
                        </li>
                        <li>
                            <i class="fas fa-clock"></i>
                            <div>Lun-Ven: 9:00 - 18:00<br>Sab: 10:00 - 14:00</div>
                        </li>
                    </ul>
                </div>
                
                <div class="contact-form">
                    <h3>Inviaci un Messaggio</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Nome e Cognome</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="subject">Oggetto</label>
                            <input type="text" id="subject" class="form-control" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Messaggio</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn btn-primary">Invia Messaggio</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-col">
                    <h4>EuroTeam B2B Services</h4>
                    <p>Soluzioni business innovative e servizi di qualità per professionisti e aziende in Romania e Italia.</p>
                    <div class="social-links">
                        <a href="https://www.facebook.com/euroteamadvices"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h4>Servizi</h4>
                    <ul class="footer-links">
                        <li><a href="#service-detail-1" data-service="1">Sede Legale</a></li>
                        <li><a href="#service-detail-2" data-service="2">Ufficio Virtuale</a></li>
                        <li><a href="#service-detail-3" data-service="3">Servizi E-commerce</a></li>
                        <li><a href="#service-detail-4" data-service="4">Assistenza Banche</a></li>
                        <li><a href="#">Organizzazione Eventi</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h4>Link Utili</h4>
                    <ul class="footer-links">
                        <li><a href="#">Chi Siamo</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">FAQ</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Termini e Condizioni</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h4>Newsletter</h4>
                    <p>Iscriviti alla nostra newsletter per ricevere aggiornamenti e offerte speciali.</p>
                    <form class="newsletter-form">
                        <input type="email" placeholder="La tua email" class="form-control">
                        <button type="submit" class="btn btn-primary">Iscriviti</button>
                    </form>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 EuroTeam B2B Services Srl. Tutti i diritti riservati.</p>
            </div>
        </div>
    </footer>

    <!-- Pagine di dettaglio servizi (nascoste inizialmente) -->
    <div id="service-detail-1" class="service-detail-page">
        <div class="service-detail-content">
            <div class="service-detail-header">
                <h2>Sede Legale</h2>
                <p>Servizi completi per la registrazione e gestione della tua società in Romania</p>
                <div class="service-detail-close">
                    <i class="fas fa-times"></i>
                </div>
            </div>
            <div class="service-detail-body">
                <img src="https://images.unsplash.com/photo-1560472355-536de3962603?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80" alt="Sede Legale" class="service-detail-image">
                
                <h3>Servizio di Sede Legale Completo</h3>
                <p>Offriamo un servizio completo di sede legale per la tua società in Romania, con indirizzo prestigioso a Bucarest e tutti i servizi amministrativi necessari per operare in conformità con le normative locali.</p>
                
                <div class="service-features">
                    <h4>Cosa include il servizio:</h4>
                    <ul>
                        <li><i class="fas fa-check-circle"></i> Indirizzo prestigioso nel centro di Bucarest</li>
                        <li><i class="fas fa-check-circle"></i> Ricezione e inoltro della corrispondenza</li>
                        <li><i class="fas fa-check-circle"></i> Servizio de segreteria telefonica</li>
                        <li><i class="fas fa-check-circle"></i> Supporto per pratiche amministrative</li>
                        <li><i class="fas fa-check-circle"></i> Assistenza in 5 lingue</li>
                    </ul>
                </div>
                
                <div class="service-detail-cta">
                    <h3>Pronto per iniziare?</h3>
                    <p>Contattaci oggi stesso per maggiori informazioni o per attivare il servizio</p>
                    <a href="#contact" class="btn btn-primary">Richiedi informazioni</a>
                </div>
            </div>
        </div>
    </div>

    <div id="service-detail-2" class="service-detail-page">
        <div class="service-detail-content">
            <div class="service-detail-header">
                <h2>Ufficio Virtuale</h2>
                <p>Tutti i vantaggi di un ufficio fisico senza i costi fissi</p>
                <div class="service-detail-close">
                    <i class="fas fa-times"></i>
                </div>
            </div>
            <div class="service-detail-body">
                <img src="https://images.unsplash.com/photo-1577375729152-4c8b5fcda381?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80" alt="Ufficio Virtuale" class="service-detail-image">
                
                <h3>Ufficio Virtuale Completo</h3>
                <p>Il nostro servizio di ufficio virtuale ti permette di avere una presenza professionale in Romania senza i costi fissi di un ufficio fisico. Perfetto per freelancer, startup e aziende che vogliono espandersi nel mercato rumeno.</p>
                
                <div class="service-features">
                    <h4>Cosa include il servizio:</h4>
                    <ul>
                        <li><i class="fas fa-check-circle"></i> Indirizzo commerciale prestigioso</li>
                        <li><i class="fas fa-check-circle"></i> Ricezione e gestione corrispondenza</li>
                        <li><i class="fas fa-check-circle"></i> Servizio di segreteria telefonica personalizzato</li>
                        <li><i class="fas fa-check-circle"></i> Supporto amministrativo dedicato</li>
                        <li><i class="fas fa-check-circle"></i> Accesso a sale riunioni (a ore)</li>
                    </ul>
                </div>
                
                <div class="service-detail-cta">
                    <h3>Pronto per iniziare?</h3>
                    <p>Contattaci oggi stesso per maggiori informazioni o per attivare il servizio</p>
                    <a href="#contact" class="btn btn-primary">Richiedi informazioni</a>
                </div>
            </div>
        </div>
    </div>

    <div id="service-detail-3" class="service-detail-page">
        <div class="service-detail-content">
            <div class="service-detail-header">
                <h2>Servizi E-commerce</h2>
                <p>Soluzioni complete per il tuo business online</p>
                <div class="service-detail-close">
                    <i class="fas fa-times"></i>
                </div>
            </div>
            <div class="service-detail-body">
                <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80" alt="E-commerce Services" class="service-detail-image">
                
                <h3>Servizi E-commerce Completi</h3>
                <p>Offriamo soluzioni complete per il commercio elettronico, dalla consulenza iniziale alla gestione delle piattaforme, dal marketing digitale alla logistica. Tutto ciò di cui hai bisogno per far crescere il tuo business online.</p>
                
                <div class="service-features">
                    <h4>Cosa include il servizio:</h4>
                    <ul>
                        <li><i class="fas fa-check-circle"></i> Consulenza e-commerce specialistica</li>
                        <li><i class="fas fa-check-circle"></i> Setup e gestione piattaforme</li>
                        <li><i class="fas fa-check-circle"></i> Marketing digitale e SEO</li>
                        <li><i class="fas fa-check-circle"></i> Gestione logistica e magazzino</li>
                        <li><i class="fas fa-check-circle"></i> Supporto clienti multilingue</li>
                    </ul>
                </div>
                
                <div class="service-detail-cta">
                    <h3>Pronto per iniziare?</h3>
                    <p>Contattaci oggi stesso per maggiori informazioni o per attivare il servizio</p>
                    <a href="#contact" class="btn btn-primary">Richiedi informazioni</a>
                </div>
            </div>
        </div>
    </div>

    <!-- Nuova pagina di dettaglio per Assistenza Banche -->
    <div id="service-detail-4" class="service-detail-page">
        <div class="service-detail-content">
            <div class="service-detail-header">
                <h2>Assistenza Banche</h2>
                <p>Servizi completi per operazioni bancarie in Romania</p>
                <div class="service-detail-close">
                    <i class="fas fa-times"></i>
                </div>
            </div>
            <div class="service-detail-body">
                <img src="https://images.unsplash.com/photo-1553729459-efe14ef6055d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80" alt="Assistenza Banche" class="service-detail-image">
                
                <h3>Assistenza Completa per Operazioni Bancarie</h3>
                <p>Offriamo supporto specializzato per tutte le operazioni bancarie in Romania, dall'apertura di conti correnti alla gestione di pratiche complesse. Il nostro team esperto ti guiderà attraverso tutto il processo, garantendo tempi rapidi e massima efficienza.</p>
                
                <div class="service-features">
                    <h4>Cosa include il servizio:</h4>
                    <ul>
                        <li><i class="fas fa-check-circle"></i> Apertura conti correnti per privati e aziende</li>
                        <li><i class="fas fa-check-circle"></i> Assistenza per ottenere linee di credito e finanziamenti</li>
                        <li><i class="fas fa-check-circle"></i> Supporto per operazioni bancarie internazionali</li>
                        <li><i class="fas fa-check-circle"></i> Gestione pratiche con istituti bancari rumeni</li>
                        <li><i class="fas fa-check-circle"></i> Consulenza per ottimizzare le operazioni finanziarie</li>
                        <li><i class="fas fa-check-circle"></i> Assistenza in 5 lingue con personale specializzato</li>
                    </ul>
                </div>
                
                <div class="service-detail-cta">
                    <h3>Pronto per iniziare?</h3>
                    <p>Contattaci oggi stesso per maggiori informazioni o per attivare il servizio</p>
                    <a href="#contact" class="btn btn-primary">Richiedi informazioni</a>
                </div>
            </div>
        </div>
    </div>

    <!-- AI Chat Widget -->
    <div class="chat-widget">
        <div class="chat-button">
            <i class="fas fa-comments"></i>
        </div>
        
        <div class="chat-container">
            <div class="chat-header">
                <h3><i class="fas fa-robot"></i> Assistente Virtuale <span class="language-indicator">48 lingue</span></h3>
                <button class="chat-close">
                    <i class="fas fa-times"></i>
                </button>
            </div>
            
            <div class="chat-messages">
                <div class="message bot">
                    <div class="message-avatar">
                        <i class="fas fa-robot"></i>
                    </div>
                    <div class="message-content">
                        Ciao! Sono l'assistente virtuale di EuroTeam. Posso rispondere alle tue domande in 48 lingue. Come posso aiutarti oggi?
                    </div>
                </div>
            </div>
            
            <div class="chat-input-container">
                <select class="language-select">
                    <option>Italiano</option>
                    <option>English</option>
                    <option>Română</option>
                    <option>Español</option>
                    <option>Français</option>
                    <option>Deutsch</option>
                </select>
                <input type="text" class="chat-input" placeholder="Scrivi un messaggio...">
                <button class="chat-send"><i class="fas fa-paper-plane"></i></button>
            </div>
        </div>
    </div>

    <script>
        // Menu toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');
        
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            menuToggle.innerHTML = navLinks.classList.contains('active') ? 
                '<i class="fas fa-times"></i>' : '<i class="fas fa-bars"></i>';
        });
        
        // Scroll animations
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.feature-card, .service-card').forEach(card => {
            observer.observe(card);
        });
        
        // Stats counter animation
        const counters = document.querySelectorAll('.stat-number');
        const speed = 200;
        
        const animateCounters = () => {
            counters.forEach(counter => {
                const target = +counter.getAttribute('data-count');
                const count = +counter.innerText;
                const increment = Math.ceil(target / speed);
                
                if (count < target) {
                    counter.innerText = count + increment;
                    setTimeout(() => animateCounters(), 1);
                } else {
                    counter.innerText = target;
                }
            });
        };
        
        let counted = false;
        
        const counterSection = document.querySelector('.stats');
        window.addEventListener('scroll', () => {
            const sectionPos = counterSection.getBoundingClientRect().top;
            const screenPos = window.innerHeight / 1.3;
            
            if (sectionPos < screenPos && !counted) {
                animateCounters();
                counted = true;
            }
        });
        
        // Chat widget
        const chatButton = document.querySelector('.chat-button');
        const chatContainer = document.querySelector('.chat-container');
        const chatClose = document.querySelector('.chat-close');
        
        chatButton.addEventListener('click', () => {
            chatContainer.style.display = 'flex';
        });
        
        chatClose.addEventListener('click', () => {
            chatContainer.style.display = 'none';
        });
        
        // Simple AI chat simulation
        const chatInput = document.querySelector('.chat-input');
        const chatSend = document.querySelector('.chat-send');
        const chatMessages = document.querySelector('.chat-messages');
        const languageSelect = document.querySelector('.language-select');
        
        const botResponses = {
            'Italiano': [
                "Posso aiutarti con informazioni sui nostri servizi di ufficio virtuale?",
                "Desideri maggiori informazioni sulla sede legale a Bucarest?",
                "Posso fornirti dettagli sui nostri servizi amministrativi per aziende.",
                "Vuoi conoscere le opzioni di supporto per giovani imprenditori?",
                "Posso assisterti con informazioni sui nostri servizi e-commerce.",
                "Posso aiutarti con informazioni sulla nostra assistenza bancaria?"
            ],
            'English': [
                "Can I help you with information about our virtual office services?",
                "Would you like more information about the headquarters in Bucharest?",
                "I can provide you with details about our administrative services for businesses.",
                "Do you want to know about support options for young entrepreneurs?",
                "I can assist you with information about our e-commerce services.",
                "Can I help you with information about our banking assistance?"
            ],
            'Română': [
                "Vă pot ajuta cu informații despre serviciile noastre de office virtual?",
                "Doriți mai multe informații despre sediul din București?",
                "Vă pot oferi detalii despre serviciile noastre administrative pentru afaceri.",
                "Doriți să aflați despre opțiunile de sprijin pentru tinerii antreprenori?",
                "Vă pot ajuta cu informații despre serviciile noastre de e-commerce.",
                "Vă pot ajuta cu informații despre asistența noastră bancară?"
            ],
            'Español': [
                "¿Puedo ayudarte con información sobre nuestros servicios de oficina virtual?",
                "¿Desea más información sobre la sede en Bucarest?",
                "Puedo proporcionarle detalles sobre nuestros servicios administrativos para empresas.",
                "¿Quiere conocer las opciones de apoyo para jóvenes emprendedores?",
                "Puedo ayudarle con información sobre nuestros servicios de comercio electrónico.",
                "¿Puedo ayudarte con información sobre nuestra asistencia bancaria?"
            ],
            'Français': [
                "Puis-je vous aider avec des informations sur nos services de bureau virtuel?",
                "Souhaitez-vous plus d'informations sur le siège social de Bucarest?",
                "Je peux vous fournir des détails sur nos services administratifs pour les entreprises.",
                "Voulez-vous connaître les options de soutien pour les jeunes entrepreneurs?",
                "Je peux vous aider avec des informations sur nos services de commerce électronique.",
                "Puis-je vous aider avec des informations sur notre assistance bancaire?"
            ],
            'Deutsch': [
                "Kann ich Ihnen mit Informationen zu unseren Virtual Office-Services helfen?",
                "Möchten Sie mehr über den Hauptsitz in Bukarest erfahren?",
                "Ich kann Ihnen Details zu unseren administrativen Dienstleistungen für Unternehmen geben.",
                "Möchten Sie mehr über die Unterstützungsmöglichkeiten für junge Unternehmer erfahren?",
                "Ich kann Ihnen mit Informationen zu unseren E-Commerce-Dienstleistungen helfen.",
                "Kann ich Ihnen mit Informationen zu unserer Bankenassistenz helfen?"
            ]
        };
        
        chatSend.addEventListener('click', sendMessage);
        chatInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') sendMessage();
        });
        
        function sendMessage() {
            const message = chatInput.value.trim();
            if (message === '') return;
            
            // Add user message
            addMessage(message, 'user');
            chatInput.value = '';
            
            // Bot response after a short delay
            setTimeout(() => {
                const selectedLanguage = languageSelect.value;
                const responses = botResponses[selectedLanguage] || botResponses['Italiano'];
                const randomResponse = responses[Math.floor(Math.random() * responses.length)];
                addMessage(randomResponse, 'bot');
            }, 1000);
        }
        
        function addMessage(text, sender) {
            const messageDiv = document.createElement('div');
            messageDiv.classList.add('message', sender);
            
            const avatar = document.createElement('div');
            avatar.classList.add('message-avatar');
            avatar.innerHTML = sender === 'bot' ? 
                '<i class="fas fa-robot"></i>' : '<i class="fas fa-user"></i>';
            
            const content = document.createElement('div');
            content.classList.add('message-content');
            content.textContent = text;
            
            messageDiv.appendChild(avatar);
            messageDiv.appendChild(content);
            
            chatMessages.appendChild(messageDiv);
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }
        
        // Form submission
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Grazie per il tuo messaggio! Ti contatteremo al più presto.');
            contactForm.reset();
        });
        
        // Service detail pages
        const serviceLinks = document.querySelectorAll('[data-service]');
        const serviceDetailPages = document.querySelectorAll('.service-detail-page');
        const detailCloseButtons = document.querySelectorAll('.service-detail-close');
        
        serviceLinks.forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                const serviceId = link.getAttribute('data-service');
                const detailPage = document.getElementById(`service-detail-${serviceId}`);
                
                if (detailPage) {
                    detailPage.style.display = 'block';
                    document.body.style.overflow = 'hidden';
                }
            });
        });
        
        detailCloseButtons.forEach(button => {
            button.addEventListener('click', () => {
                serviceDetailPages.forEach(page => {
                    page.style.display = 'none';
                });
                document.body.style.overflow = 'auto';
            });
        });
        
        // Close detail page when clicking outside content
        serviceDetailPages.forEach(page => {
            page.addEventListener('click', (e) => {
                if (e.target === page) {
                    page.style.display = 'none';
                    document.body.style.overflow = 'auto';
                }
            });
        });
    </script>
</body>
</html>
