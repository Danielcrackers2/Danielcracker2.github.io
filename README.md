# Danielcracker2.github.io
hope  for life

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CrossSector Interview Platform</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, sans-serif;
        }
        
        :root {
            --primary: #3a36e0;
            --primary-dark: #261e9c;
            --secondary: #00c9a7;
            --dark: #1a1a2e;
            --light: #f8f9fa;
            --gray: #6c757d;
            --danger: #e63946;
            --warning: #ff9e00;
            --success: #2ecc71;
        }
        
        body {
            background-color: #f5f7ff;
            color: var(--dark);
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Login Page Styles */
        .login-container {
            display: flex;
            min-height: 100vh;
            align-items: center;
            justify-content: center;
            padding: 20px;
            background: linear-gradient(135deg, #f5f7ff 0%, #e3e6ff 100%);
        }
        
        .login-card {
            background: white;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 1000px;
            overflow: hidden;
            display: flex;
            min-height: 600px;
        }
        
        .login-left {
            flex: 1;
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
            padding: 50px 40px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .login-left h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        .login-left p {
            font-size: 1.1rem;
            opacity: 0.9;
            line-height: 1.6;
            margin-bottom: 30px;
        }
        
        .login-features {
            list-style: none;
            margin-top: 30px;
        }
        
        .login-features li {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .login-features i {
            margin-right: 12px;
            font-size: 1.2rem;
            color: var(--secondary);
        }
        
        .login-right {
            flex: 1;
            padding: 50px 40px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .login-tabs {
            display: flex;
            margin-bottom: 30px;
            border-bottom: 1px solid #eee;
        }
        
        .login-tab {
            padding: 15px 25px;
            font-weight: 600;
            cursor: pointer;
            color: var(--gray);
            border-bottom: 3px solid transparent;
            transition: all 0.3s;
        }
        
        .login-tab.active {
            color: var(--primary);
            border-bottom-color: var(--primary);
        }
        
        .login-form {
            display: none;
        }
        
        .login-form.active {
            display: block;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--dark);
        }
        
        .input-with-icon {
            position: relative;
        }
        
        .input-with-icon i {
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--gray);
        }
        
        .input-with-icon input {
            width: 100%;
            padding: 15px 15px 15px 45px;
            border: 2px solid #e1e5f1;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        .input-with-icon input:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(58, 54, 224, 0.1);
        }
        
        .password-toggle {
            position: absolute;
            right: 15px;
            top: 50%;
            transform: translateY(-50%);
            cursor: pointer;
            color: var(--gray);
        }
        
        .auth-method {
            display: flex;
            justify-content: space-between;
            margin-bottom: 25px;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .auth-option {
            flex: 1;
            min-width: 120px;
            padding: 12px;
            border: 2px solid #e1e5f1;
            border-radius: 10px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .auth-option:hover {
            border-color: var(--primary);
            background-color: rgba(58, 54, 224, 0.05);
        }
        
        .auth-option i {
            font-size: 1.5rem;
            margin-bottom: 8px;
            color: var(--primary);
        }
        
        .btn {
            display: inline-block;
            padding: 15px 30px;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            text-align: center;
            width: 100%;
        }
        
        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(58, 54, 224, 0.2);
        }
        
        .forgot-link {
            display: block;
            text-align: center;
            margin-top: 20px;
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
        }
        
        /* Dashboard Styles */
        .dashboard-container {
            display: none;
            min-height: 100vh;
        }
        
        .dashboard-header {
            background: white;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo i {
            margin-right: 10px;
            font-size: 2rem;
        }
        
        .user-menu {
            display: flex;
            align-items: center;
            gap: 20px;
        }
        
        .user-avatar {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 600;
            font-size: 1.2rem;
        }
        
        .dashboard-main {
            padding: 40px 0;
        }
        
        .welcome-section {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
            padding: 40px;
            border-radius: 20px;
            margin-bottom: 40px;
        }
        
        .welcome-section h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .welcome-section p {
            font-size: 1.1rem;
            opacity: 0.9;
            max-width: 600px;
        }
        
        .sector-selection {
            margin-bottom: 40px;
        }
        
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 25px;
            color: var(--dark);
        }
        
        .sectors-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
        }
        
        .sector-card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
            cursor: pointer;
            border: 2px solid transparent;
        }
        
        .sector-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            border-color: var(--primary);
        }
        
        .sector-icon {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            color: white;
            font-size: 1.8rem;
        }
        
        .sector-card h3 {
            font-size: 1.4rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .sector-card p {
            color: var(--gray);
            line-height: 1.6;
            margin-bottom: 20px;
        }
        
        .sector-stats {
            display: flex;
            justify-content: space-between;
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        .interview-types {
            margin-bottom: 40px;
        }
        
        .types-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .type-card {
            background: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
            transition: all 0.3s;
            cursor: pointer;
            text-align: center;
            border-left: 5px solid var(--primary);
        }
        
        .type-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .type-card i {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .type-card h4 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        /* Interview Interface */
        .interview-container {
            display: none;
            min-height: 100vh;
            background-color: #f8f9fa;
        }
        
        .interview-header {
            background: white;
            padding: 20px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .interview-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .interview-timer {
            background: var(--primary);
            color: white;
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.2rem;
        }
        
        .interview-main {
            padding: 40px 0;
        }
        
        .interview-card {
            background: white;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08);
            padding: 40px;
            margin-bottom: 30px;
        }
        
        .question-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid #eee;
        }
        
        .question-number {
            font-size: 1.1rem;
            color: var(--gray);
        }
        
        .question-type {
            background: var(--secondary);
            color: white;
            padding: 5px 15px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
        }
        
        .question-text {
            font-size: 1.4rem;
            line-height: 1.6;
            margin-bottom: 30px;
            color: var(--dark);
        }
        
        .options-container {
            margin-bottom: 30px;
        }
        
        .option {
            display: flex;
            align-items: center;
            padding: 20px;
            border: 2px solid #e1e5f1;
            border-radius: 10px;
            margin-bottom: 15px;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .option:hover {
            border-color: var(--primary);
            background-color: rgba(58, 54, 224, 0.05);
        }
        
        .option.selected {
            border-color: var(--primary);
            background-color: rgba(58, 54, 224, 0.1);
        }
        
        .option-radio {
            width: 22px;
            height: 22px;
            border-radius: 50%;
            border: 2px solid #ddd;
            margin-right: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .option-radio.selected::after {
            content: '';
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background-color: var(--primary);
        }
        
        .interview-controls {
            display: flex;
            justify-content: space-between;
            margin-top: 40px;
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
        }
        
        .btn-success {
            background-color: var(--success);
        }
        
        .btn-success:hover {
            background-color: #27ae60;
        }
        
        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background: white;
            border-radius: 20px;
            padding: 40px;
            max-width: 500px;
            width: 90%;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.2);
        }
        
        .modal h2 {
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .modal p {
            margin-bottom: 30px;
            color: var(--gray);
            line-height: 1.6;
        }
        
        .modal-actions {
            display: flex;
            justify-content: flex-end;
            gap: 15px;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .login-card {
                flex-direction: column;
                max-width: 600px;
            }
            
            .login-left, .login-right {
                padding: 40px 30px;
            }
        }
        
        @media (max-width: 768px) {
            .welcome-section h1 {
                font-size: 2rem;
            }
            
            .sectors-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
            
            .interview-card {
                padding: 25px;
            }
            
            .question-text {
                font-size: 1.2rem;
            }
        }
        
        @media (max-width: 576px) {
            .login-left, .login-right {
                padding: 30px 20px;
            }
            
            .auth-method {
                flex-direction: column;
            }
            
            .header-content {
                flex-direction: column;
                gap: 15px;
            }
            
            .interview-controls {
                flex-direction: column;
                gap: 15px;
            }
            
            .interview-controls .btn {
                width: 100%;
            }
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .fade-in {
            animation: fadeIn 0.5s ease-out;
        }
    </style>
</head>
<body>
    <!-- Login Container -->
    <div class="login-container" id="login-container">
        <div class="login-card fade-in">
            <div class="login-left">
                <h1>CrossSector Interview Platform</h1>
                <p>A comprehensive interviewing solution for all industries and job roles. Practice, prepare, and excel in your career journey.</p>
                
                <ul class="login-features">
                    <li><i class="fas fa-check-circle"></i> Industry-specific interview questions</li>
                    <li><i class="fas fa-check-circle"></i> Real-time feedback and scoring</li>
                    <li><i class="fas fa-check-circle"></i> Mock interviews with AI evaluation</li>
                    <li><i class="fas fa-check-circle"></i> Progress tracking and analytics</li>
                    <li><i class="fas fa-check-circle"></i> Multi-platform compatibility</li>
                </ul>
            </div>
            
            <div class="login-right">
                <div class="login-tabs">
                    <div class="login-tab active" data-tab="login">Login</div>
                    <div class="login-tab" data-tab="register">Register</div>
                    <div class="login-tab" data-tab="guest">Guest Access</div>
                </div>
                
                <!-- Login Form -->
                <form class="login-form active" id="login-form">
                    <div class="form-group">
                        <label for="login-email">Email Address</label>
                        <div class="input-with-icon">
                            <i class="fas fa-envelope"></i>
                            <input type="email" id="login-email" placeholder="Enter your email" required>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="login-password">Password</label>
                        <div class="input-with-icon">
                            <i class="fas fa-lock"></i>
                            <input type="password" id="login-password" placeholder="Enter your password" required>
                            <span class="password-toggle" id="login-password-toggle">
                                <i class="fas fa-eye"></i>
                            </span>
                        </div>
                    </div>
                    
                    <div class="auth-method">
                        <div class="auth-option" id="google-auth">
                            <i class="fab fa-google"></i>
                            <div>Google</div>
                        </div>
                        <div class="auth-option" id="linkedin-auth">
                            <i class="fab fa-linkedin"></i>
                            <div>LinkedIn</div>
                        </div>
                        <div class="auth-option" id="sso-auth">
                            <i class="fas fa-id-card"></i>
                            <div>SSO</div>
                        </div>
                    </div>
                    
                    <button type="submit" class="btn">Login to Dashboard</button>
                    
                    <a href="#" class="forgot-link" id="forgot-password">Forgot Password?</a>
                </form>
                
                <!-- Register Form -->
                <form class="login-form" id="register-form">
                    <div class="form-group">
                        <label for="register-name">Full Name</label>
                        <div class="input-with-icon">
                            <i class="fas fa-user"></i>
                            <input type="text" id="register-name" placeholder="Enter your full name" required>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="register-email">Email Address</label>
                        <div class="input-with-icon">
                            <i class="fas fa-envelope"></i>
                            <input type="email" id="register-email" placeholder="Enter your email" required>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="register-password">Password</label>
                        <div class="input-with-icon">
                            <i class="fas fa-lock"></i>
                            <input type="password" id="register-password" placeholder="Create a password" required>
                            <span class="password-toggle" id="register-password-toggle">
                                <i class="fas fa-eye"></i>
                            </span>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="register-confirm-password">Confirm Password</label>
                        <div class="input-with-icon">
                            <i class="fas fa-lock"></i>
                            <input type="password" id="register-confirm-password" placeholder="Confirm your password" required>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label>Role</label>
                        <div class="auth-method">
                            <div class="auth-option role-option active" data-role="candidate">
                                <i class="fas fa-user-tie"></i>
                                <div>Candidate</div>
                            </div>
                            <div class="auth-option role-option" data-role="interviewer">
                                <i class="fas fa-clipboard-check"></i>
                                <div>Interviewer</div>
                            </div>
                            <div class="auth-option role-option" data-role="admin">
                                <i class="fas fa-cog"></i>
                                <div>Admin</div>
                            </div>
                        </div>
                    </div>
                    
                    <button type="submit" class="btn">Create Account</button>
                </form>
                
                <!-- Guest Access Form -->
                <form class="login-form" id="guest-form">
                    <div class="form-group">
                        <label for="guest-name">Your Name</label>
                        <div class="input-with-icon">
                            <i class="fas fa-user"></i>
                            <input type="text" id="guest-name" placeholder="Enter your name" required>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="guest-sector">Sector of Interest</label>
                        <div class="input-with-icon">
                            <i class="fas fa-industry"></i>
                            <select id="guest-sector" style="width: 100%; padding: 15px 15px 15px 45px; border: 2px solid #e1e5f1; border-radius: 10px; font-size: 1rem;">
                                <option value="">Select a sector</option>
                                <option value="tech">Technology</option>
                                <option value="finance">Finance</option>
                                <option value="healthcare">Healthcare</option>
                                <option value="marketing">Marketing</option>
                            </select>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label>Interview Type</label>
                        <div class="auth-method">
                            <div class="auth-option interview-type active" data-type="practice">
                                <i class="fas fa-dumbbell"></i>
                                <div>Practice</div>
                            </div>
                            <div class="auth-option interview-type" data-type="mock">
                                <i class="fas fa-video"></i>
                                <div>Mock</div>
                            </div>
                            <div class="auth-option interview-type" data-type="assessment">
                                <i class="fas fa-clipboard-list"></i>
                                <div>Assessment</div>
                            </div>
                        </div>
                    </div>
                    
                    <button type="submit" class="btn">Start as Guest</button>
                    
                    <p style="text-align: center; margin-top: 20px; font-size: 0.9rem; color: var(--gray);">
                        Guest access is limited to 3 interviews per day
                    </p>
                </form>
            </div>
        </div>
    </div>
    
    <!-- Dashboard Container -->
    <div class="dashboard-container" id="dashboard-container">
        <header class="dashboard-header">
            <div class="container">
                <div class="header-content">
                    <div class="logo">
                        <i class="fas fa-comments"></i>
                        CrossSector
                    </div>
                    
                    <div class="user-menu">
                        <div class="user-avatar" id="user-avatar">JD</div>
                        <div>
                            <div id="user-name">John Doe</div>
                            <div style="font-size: 0.9rem; color: var(--gray);" id="user-role">Candidate</div>
                        </div>
                        <button class="btn btn-outline" id="logout-btn" style="width: auto; padding: 10px 20px;">
                            <i class="fas fa-sign-out-alt"></i> Logout
                        </button>
                    </div>
                </div>
            </div>
        </header>
        
        <main class="dashboard-main">
            <div class="container">
                <section class="welcome-section fade-in">
                    <h1>Welcome back, <span id="welcome-name">John</span>!</h1>
                    <p>Ready to ace your next interview? Select a sector below to begin your preparation journey.</p>
                </section>
                
                <section class="sector-selection">
                    <h2 class="section-title">Select Interview Sector</h2>
                    
                    <div class="sectors-grid">
                        <!-- Technology Sector -->
                        <div class="sector-card" data-sector="technology">
                            <div class="sector-icon">
                                <i class="fas fa-laptop-code"></i>
                            </div>
                            <h3>Technology</h3>
                            <p>Software engineering, data science, cybersecurity, IT support, and product management interviews.</p>
                            <div class="sector-stats">
                                <span><i class="fas fa-question-circle"></i> 250+ questions</span>
                                <span><i class="fas fa-clock"></i> 45-60 min</span>
                            </div>
                        </div>
                        
                        <!-- Finance Sector -->
                        <div class="sector-card" data-sector="finance">
                            <div class="sector-icon">
                                <i class="fas fa-chart-line"></i>
                            </div>
                            <h3>Finance</h3>
                            <p>Investment banking, accounting, financial analysis, risk management, and fintech interviews.</p>
                            <div class="sector-stats">
                                <span><i class="fas fa-question-circle"></i> 180+ questions</span>
                                <span><i class="fas fa-clock"></i> 40-55 min</span>
                            </div>
                        </div>
                        
                        <!-- Healthcare Sector -->
                        <div class="sector-card" data-sector="healthcare">
                            <div class="sector-icon">
                                <i class="fas fa-heartbeat"></i>
                            </div>
                            <h3>Healthcare</h3>
                            <p>Medical, nursing, pharmaceutical, healthcare administration, and biotechnology interviews.</p>
                            <div class="sector-stats">
                                <span><i class="fas fa-question-circle"></i> 220+ questions</span>
                                <span><i class="fas fa-clock"></i> 50-70 min</span>
                            </div>
                        </div>
                        
                        <!-- Marketing Sector -->
                        <div class="sector-card" data-sector="marketing">
                            <div class="sector-icon">
                                <i class="fas fa-bullhorn"></i>
                            </div>
                            <h3>Marketing</h3>
                            <p>Digital marketing, brand management, market research, advertising, and PR interviews.</p>
                            <div class="sector-stats">
                                <span><i class="fas fa-question-circle"></i> 160+ questions</span>
                                <span><i class="fas fa-clock"></i> 35-50 min</span>
                            </div>
                        </div>
                    </div>
                </section>
                
                <section class="interview-types">
                    <h2 class="section-title">Interview Types</h2>
                    
                    <div class="types-grid">
                        <div class="type-card" data-interview-type="practice">
                            <i class="fas fa-dumbbell"></i>
                            <h4>Practice Mode</h4>
                            <p>Self-paced practice with instant feedback</p>
                        </div>
                        
                        <div class="type-card" data-interview-type="mock">
                            <i class="fas fa-video"></i>
                            <h4>Mock Interview</h4>
                            <p>Simulated interview with AI evaluation</p>
                        </div>
                        
                        <div class="type-card" data-interview-type="assessment">
                            <i class="fas fa-clipboard-list"></i>
                            <h4>Skill Assessment</h4>
                            <p>Technical tests and competency evaluation</p>
                        </div>
                        
                        <div class="type-card" data-interview-type="behavioral">
                            <i class="fas fa-users"></i>
                            <h4>Behavioral Interview</h4>
                            <p>Soft skills and situational judgment tests</p>
                        </div>
                    </div>
                </section>
            </div>
        </main>
    </div>
    
    <!-- Interview Container -->
    <div class="interview-container" id="interview-container">
        <header class="interview-header">
            <div class="container">
                <div class="interview-info">
                    <div>
                        <h2 id="interview-sector">Technology Interview</h2>
                        <p id="interview-type">Practice Mode</p>
                    </div>
                    <div class="interview-timer">
                        <i class="fas fa-clock"></i> <span id="timer">45:00</span>
                    </div>
                </div>
            </div>
        </header>
        
        <main class="interview-main">
            <div class="container">
                <div class="interview-card fade-in">
                    <div class="question-header">
                        <div class="question-number">Question 1 of 10</div>
                        <div class="question-type" id="current-question-type">Technical</div>
                    </div>
                    
                    <div class="question-text" id="question-text">
                        Explain the difference between let, const, and var in JavaScript. What are the key considerations when choosing which one to use?
                    </div>
                    
                    <div class="options-container" id="options-container">
                        <!-- Options will be populated by JavaScript -->
                    </div>
                    
                    <div class="interview-controls">
                        <button class="btn btn-outline" id="prev-question">
                            <i class="fas fa-arrow-left"></i> Previous
                        </button>
                        
                        <div>
                            <button class="btn btn-outline" id="skip-question">
                                Skip Question
                            </button>
                            <button class="btn" id="next-question">
                                Next Question <i class="fas fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <div class="interview-controls">
                    <button class="btn btn-outline" id="exit-interview">
                        <i class="fas fa-sign-out-alt"></i> Exit Interview
                    </button>
                    
                    <button class="btn btn-success" id="submit-interview">
                        <i class="fas fa-paper-plane"></i> Submit Interview
                    </button>
                </div>
            </div>
        </main>
    </div>
    
    <!-- Confirmation Modal -->
    <div class="modal" id="confirmation-modal">
        <div class="modal-content">
            <h2>Submit Interview?</h2>
            <p>You have completed 3 out of 10 questions. Are you sure you want to submit your interview now? You cannot return to this interview once submitted.</p>
            <div class="modal-actions">
                <button class="btn btn-outline" id="cancel-submit">Cancel</button>
                <button class="btn" id="confirm-submit">Yes, Submit</button>
            </div>
        </div>
    </div>
    
    <script>
        // DOM Elements
        const loginContainer = document.getElementById('login-container');
        const dashboardContainer = document.getElementById('dashboard-container');
        const interviewContainer = document.getElementById('interview-container');
        const confirmationModal = document.getElementById('confirmation-modal');
        
        // Login elements
        const loginTabs = document.querySelectorAll('.login-tab');
        const loginForms = document.querySelectorAll('.login-form');
        const passwordToggles = document.querySelectorAll('.password-toggle');
        const roleOptions = document.querySelectorAll('.role-option');
        const interviewTypeOptions = document.querySelectorAll('.interview-type');
        const authOptions = document.querySelectorAll('.auth-option');
        const loginForm = document.getElementById('login-form');
        const registerForm = document.getElementById('register-form');
        const guestForm = document.getElementById('guest-form');
        
        // Dashboard elements
        const sectorCards = document.querySelectorAll('.sector-card');
        const typeCards = document.querySelectorAll('.type-card');
        const logoutBtn = document.getElementById('logout-btn');
        const userAvatar = document.getElementById('user-avatar');
        const userName = document.getElementById('user-name');
        const userRole = document.getElementById('user-role');
        const welcomeName = document.getElementById('welcome-name');
        
        // Interview elements
        const interviewSector = document.getElementById('interview-sector');
        const interviewType = document.getElementById('interview-type');
        const timerElement = document.getElementById('timer');
        const questionText = document.getElementById('question-text');
        const optionsContainer = document.getElementById('options-container');
        const prevQuestionBtn = document.getElementById('prev-question');
        const nextQuestionBtn = document.getElementById('next-question');
        const skipQuestionBtn = document.getElementById('skip-question');
        const exitInterviewBtn = document.getElementById('exit-interview');
        const submitInterviewBtn = document.getElementById('submit-interview');
        const cancelSubmitBtn = document.getElementById('cancel-submit');
        const confirmSubmitBtn = document.getElementById('confirm-submit');
        
        // State variables
        let currentUser = {
            name: 'John Doe',
            role: 'candidate',
            email: 'john.doe@example.com'
        };
        
        let selectedSector = '';
        let selectedInterviewType = '';
        let currentQuestionIndex = 0;
        let timerInterval;
        let timeLeft = 45 * 60; // 45 minutes in seconds
        
        // Questions data for different sectors
        const questionsData = {
            technology: [
                {
                    type: 'Technical',
                    text: 'Explain the difference between let, const, and var in JavaScript. What are the key considerations when choosing which one to use?',
                    options: [
                        'var is function-scoped, let and const are block-scoped. const cannot be reassigned.',
                        'All three are identical in functionality, just different syntax.',
                        'let and var are for variables, const is for constants. All are function-scoped.',
                        'var is for global variables, let for local, const for constants. All are hoisted the same way.'
                    ],
                    correctAnswer: 0
                },
                {
                    type: 'Technical',
                    text: 'What is the time complexity of a binary search algorithm?',
                    options: [
                        'O(log n)',
                        'O(n)',
                        'O(n log n)',
                        'O(1)'
                    ],
                    correctAnswer: 0
                },
                {
                    type: 'Behavioral',
                    text: 'Describe a time when you had to learn a new technology quickly to complete a project.',
                    options: [],
                    correctAnswer: -1 // Open-ended question
                }
            ],
            finance: [
                {
                    type: 'Technical',
                    text: 'What is the difference between EBITDA and net income?',
                    options: [
                        'EBITDA excludes interest, taxes, depreciation, and amortization, while net income includes all expenses.',
                        'EBITDA is a GAAP measure, while net income is non-GAAP.',
                        'Net income is operating income minus taxes, while EBITDA is revenue minus COGS.',
                        'They are essentially the same metric with different names.'
                    ],
                    correctAnswer: 0
                },
                {
                    type: 'Technical',
                    text: 'What does WACC stand for and how is it used in finance?',
                    options: [
                        'Weighted Average Cost of Capital - used as a discount rate for DCF analysis',
                        'Weighted Average Capital Cost - used to calculate depreciation',
                        'Working Average Capital Cost - used in working capital management',
                        'Weighted Asset Cost Calculation - used in portfolio management'
                    ],
                    correctAnswer: 0
                }
            ],
            healthcare: [
                {
                    type: 'Technical',
                    text: 'What are the key components of SOAP notes in medical documentation?',
                    options: [
                        'Subjective, Objective, Assessment, Plan',
                        'Symptoms, Observations, Analysis, Prescription',
                        'Summary, Objective, Assessment, Procedure',
                        'Subjective, Objective, Analysis, Prognosis'
                    ],
                    correctAnswer: 0
                }
            ],
            marketing: [
                {
                    type: 'Technical',
                    text: 'What is the difference between SEO and SEM?',
                    options: [
                        'SEO is organic search optimization, SEM includes both organic and paid search',
                        'SEO is for search engines, SEM is for social media',
                        'SEM is a subset of SEO focusing on paid advertising',
                        'They are interchangeable terms for the same practice'
                    ],
                    correctAnswer: 0
                }
            ]
        };
        
        // Initialize the application
        function init() {
            setupEventListeners();
            showLogin();
        }
        
        // Set up event listeners
        function setupEventListeners() {
            // Login tab switching
            loginTabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    const tabId = tab.getAttribute('data-tab');
                    switchLoginTab(tabId);
                });
            });
            
            // Password toggle
            passwordToggles.forEach(toggle => {
                toggle.addEventListener('click', function() {
                    const input = this.parentElement.querySelector('input');
                    const icon = this.querySelector('i');
                    
                    if (input.type === 'password') {
                        input.type = 'text';
                        icon.classList.remove('fa-eye');
                        icon.classList.add('fa-eye-slash');
                    } else {
                        input.type = 'password';
                        icon.classList.remove('fa-eye-slash');
                        icon.classList.add('fa-eye');
                    }
                });
            });
            
            // Role selection
            roleOptions.forEach(option => {
                option.addEventListener('click', function() {
                    roleOptions.forEach(opt => opt.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Interview type selection
            interviewTypeOptions.forEach(option => {
                option.addEventListener('click', function() {
                    interviewTypeOptions.forEach(opt => opt.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Auth options
            authOptions.forEach(option => {
                option.addEventListener('click', function() {
                    // Visual feedback for selected auth method
                    authOptions.forEach(opt => opt.style.borderColor = '#e1e5f1');
                    this.style.borderColor = 'var(--primary)';
                    
                    // In a real app, this would trigger the specific authentication flow
                    if (this.id === 'google-auth') {
                        showMessage('Google authentication would open in a real application');
                    } else if (this.id === 'linkedin-auth') {
                        showMessage('LinkedIn authentication would open in a real application');
                    } else if (this.id === 'sso-auth') {
                        showMessage('Single Sign-On would open in a real application');
                    }
                });
            });
            
            // Form submissions
            loginForm.addEventListener('submit', function(e) {
                e.preventDefault();
                handleLogin();
            });
            
            registerForm.addEventListener('submit', function(e) {
                e.preventDefault();
                handleRegistration();
            });
            
            guestForm.addEventListener('submit', function(e) {
                e.preventDefault();
                handleGuestAccess();
            });
            
            // Dashboard sector selection
            sectorCards.forEach(card => {
                card.addEventListener('click', function() {
                    selectedSector = this.getAttribute('data-sector');
                    showMessage(`Selected ${selectedSector} sector`);
                    
                    // Highlight selected sector
                    sectorCards.forEach(c => c.style.borderColor = 'transparent');
                    this.style.borderColor = 'var(--primary)';
                });
            });
            
            // Dashboard interview type selection
            typeCards.forEach(card => {
                card.addEventListener('click', function() {
                    selectedInterviewType = this.getAttribute('data-interview-type');
                    
                    // Check if a sector is selected
                    if (!selectedSector) {
                        showMessage('Please select a sector first');
                        return;
                    }
                    
                    // Start the interview
                    startInterview(selectedSector, selectedInterviewType);
                });
            });
            
            // Logout button
            logoutBtn.addEventListener('click', showLogin);
            
            // Interview navigation
            prevQuestionBtn.addEventListener('click', showPreviousQuestion);
            nextQuestionBtn.addEventListener('click', showNextQuestion);
            skipQuestionBtn.addEventListener('click', skipQuestion);
            
            // Interview controls
            exitInterviewBtn.addEventListener('click', () => {
                showDashboard();
                stopTimer();
            });
            
            submitInterviewBtn.addEventListener('click', () => {
                confirmationModal.style.display = 'flex';
            });
            
            cancelSubmitBtn.addEventListener('click', () => {
                confirmationModal.style.display = 'none';
            });
            
            confirmSubmitBtn.addEventListener('click', () => {
                confirmationModal.style.display = 'none';
                showMessage('Interview submitted successfully!');
                showDashboard();
                stopTimer();
            });
            
            // Forgot password link
            document.getElementById('forgot-password').addEventListener('click', function(e) {
                e.preventDefault();
                showMessage('Password reset functionality would open in a real application');
            });
        }
        
        // Switch between login tabs
        function switchLoginTab(tabId) {
            // Update active tab
            loginTabs.forEach(tab => {
                if (tab.getAttribute('data-tab') === tabId) {
                    tab.classList.add('active');
                } else {
                    tab.classList.remove('active');
                }
            });
            
            // Show active form
            loginForms.forEach(form => {
                if (form.id === `${tabId}-form`) {
                    form.classList.add('active');
                } else {
                    form.classList.remove('active');
                }
            });
        }
        
        // Handle login
        function handleLogin() {
            const email = document.getElementById('login-email').value;
            const password = document.getElementById('login-password').value;
            
            if (!email || !password) {
                showMessage('Please fill in all fields');
                return;
            }
            
            // In a real app, this would validate credentials with a backend
            currentUser = {
                name: email.split('@')[0],
                email: email,
                role: 'candidate'
            };
            
            showDashboard();
            showMessage('Login successful!');
        }
        
        // Handle registration
        function handleRegistration() {
            const name = document.getElementById('register-name').value;
            const email = document.getElementById('register-email').value;
            const password = document.getElementById('register-password').value;
            const confirmPassword = document.getElementById('register-confirm-password').value;
            const role = document.querySelector('.role-option.active').getAttribute('data-role');
            
            if (!name || !email || !password || !confirmPassword) {
                showMessage('Please fill in all fields');
                return;
            }
            
            if (password !== confirmPassword) {
                showMessage('Passwords do not match');
                return;
            }
            
            // In a real app, this would create an account via backend
            currentUser = {
                name: name,
                email: email,
                role: role
            };
            
            showDashboard();
            showMessage('Registration successful!');
        }
        
        // Handle guest access
        function handleGuestAccess() {
            const name = document.getElementById('guest-name').value;
            const sector = document.getElementById('guest-sector').value;
            const interviewType = document.querySelector('.interview-type.active').getAttribute('data-type');
            
            if (!name || !sector) {
                showMessage('Please fill in all fields');
                return;
            }
            
            // Set guest user
            currentUser = {
                name: name,
                email: 'guest@example.com',
                role: 'guest'
            };
            
            selectedSector = sector;
            selectedInterviewType = interviewType;
            
            startInterview(selectedSector, selectedInterviewType);
        }
        
        // Show login page
        function showLogin() {
            loginContainer.style.display = 'flex';
            dashboardContainer.style.display = 'none';
            interviewContainer.style.display = 'none';
            
            // Reset forms
            switchLoginTab('login');
        }
        
        // Show dashboard
        function showDashboard() {
            loginContainer.style.display = 'none';
            dashboardContainer.style.display = 'block';
            interviewContainer.style.display = 'none';
            
            // Update user info
            userName.textContent = currentUser.name;
            userRole.textContent = currentUser.role.charAt(0).toUpperCase() + currentUser.role.slice(1);
            welcomeName.textContent = currentUser.name.split(' ')[0];
            
            // Set avatar initials
            const initials = currentUser.name.split(' ').map(n => n[0]).join('').toUpperCase();
            userAvatar.textContent = initials;
            
            // Reset selections
            selectedSector = '';
            selectedInterviewType = '';
            sectorCards.forEach(card => card.style.borderColor = 'transparent');
        }
        
        // Start interview
        function startInterview(sector, interviewType) {
            // Set interview details
            interviewSector.textContent = `${sector.charAt(0).toUpperCase() + sector.slice(1)} Interview`;
            interviewTypeElement.textContent = `${interviewType.charAt(0).toUpperCase() + interviewType.slice(1)} Mode`;
            
            // Reset question index
            currentQuestionIndex = 0;
            
            // Reset timer
            timeLeft = 45 * 60; // 45 minutes
            updateTimerDisplay();
            
            // Start timer
            startTimer();
            
            // Load first question
            loadQuestion();
            
            // Show interview interface
            loginContainer.style.display = 'none';
            dashboardContainer.style.display = 'none';
            interviewContainer.style.display = 'block';
        }
        
        // Start the interview timer
        function startTimer() {
            stopTimer(); // Clear any existing timer
            
            timerInterval = setInterval(() => {
                timeLeft--;
                updateTimerDisplay();
                
                if (timeLeft <= 0) {
                    stopTimer();
                    showMessage('Time is up!');
                    // Auto-submit in a real application
                }
            }, 1000);
        }
        
        // Stop the interview timer
        function stopTimer() {
            if (timerInterval) {
                clearInterval(timerInterval);
                timerInterval = null;
            }
        }
        
        // Update timer display
        function updateTimerDisplay() {
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            timerElement.textContent = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
            
            // Change color when time is running low
            if (timeLeft < 5 * 60) { // Less than 5 minutes
                timerElement.style.color = '#e63946';
            }
        }
        
        // Load current question
        function loadQuestion() {
            const questions = questionsData[selectedSector] || questionsData.technology;
            
            if (currentQuestionIndex >= questions.length) {
                // No more questions, end interview
                showMessage('You have completed all questions!');
                confirmationModal.style.display = 'flex';
                return;
            }
            
            const question = questions[currentQuestionIndex];
            
            // Update question text and type
            questionText.textContent = question.text;
            document.getElementById('current-question-type').textContent = question.type;
            
            // Update question number
            document.querySelector('.question-number').textContent = `Question ${currentQuestionIndex + 1} of ${questions.length}`;
            
            // Clear previous options
            optionsContainer.innerHTML = '';
            
            // If it's an open-ended question (no options)
            if (question.options.length === 0) {
                const textarea = document.createElement('textarea');
                textarea.placeholder = 'Type your answer here...';
                textarea.style.width = '100%';
                textarea.style.padding = '15px';
                textarea.style.border = '2px solid #e1e5f1';
                textarea.style.borderRadius = '10px';
                textarea.style.fontSize = '1rem';
                textarea.style.minHeight = '150px';
                textarea.style.marginTop = '20px';
                
                optionsContainer.appendChild(textarea);
                return;
            }
            
            // Create options for multiple choice questions
            question.options.forEach((option, index) => {
                const optionElement = document.createElement('div');
                optionElement.className = 'option';
                optionElement.dataset.index = index;
                
                optionElement.innerHTML = `
                    <div class="option-radio"></div>
                    <div>${option}</div>
                `;
                
                optionElement.addEventListener('click', () => {
                    // Deselect all options
                    document.querySelectorAll('.option').forEach(opt => {
                        opt.classList.remove('selected');
                        opt.querySelector('.option-radio').classList.remove('selected');
                    });
                    
                    // Select clicked option
                    optionElement.classList.add('selected');
                    optionElement.querySelector('.option-radio').classList.add('selected');
                });
                
                optionsContainer.appendChild(optionElement);
            });
            
            // Update navigation buttons
            prevQuestionBtn.disabled = currentQuestionIndex === 0;
            nextQuestionBtn.textContent = currentQuestionIndex === questions.length - 1 
                ? 'Finish Interview' 
                : 'Next Question <i class="fas fa-arrow-right"></i>';
        }
        
        // Show next question
        function showNextQuestion() {
            const questions = questionsData[selectedSector] || questionsData.technology;
            
            if (currentQuestionIndex < questions.length - 1) {
                currentQuestionIndex++;
                loadQuestion();
            } else {
                // Last question, show submit modal
                confirmationModal.style.display = 'flex';
            }
        }
        
        // Show previous question
        function showPreviousQuestion() {
            if (currentQuestionIndex > 0) {
                currentQuestionIndex--;
                loadQuestion();
            }
        }
        
        // Skip current question
        function skipQuestion() {
            const questions = questionsData[selectedSector] || questionsData.technology;
            
            if (currentQuestionIndex < questions.length - 1) {
                currentQuestionIndex++;
                loadQuestion();
                showMessage('Question skipped');
            } else {
                showMessage('This is the last question');
            }
        }
        
        // Show message (toast notification)
        function showMessage(message) {
            // Create toast element
            const toast = document.createElement('div');
            toast.textContent = message;
            toast.style.position = 'fixed';
            toast.style.bottom = '20px';
            toast.style.right = '20px';
            toast.style.backgroundColor = 'var(--dark)';
            toast.style.color = 'white';
            toast.style.padding = '15px 25px';
            toast.style.borderRadius = '10px';
            toast.style.zIndex = '1000';
            toast.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.2)';
            toast.style.fontWeight = '500';
            
            document.body.appendChild(toast);
            
            // Remove toast after 3 seconds
            setTimeout(() => {
                toast.style.opacity = '0';
                toast.style.transition = 'opacity 0.5s';
                setTimeout(() => {
                    document.body.removeChild(toast);
                }, 500);
            }, 3000);
        }
        
        // Initialize the app
        document.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>
