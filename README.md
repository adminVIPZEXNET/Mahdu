<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LINK VIPZEXNET</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2980b9;
            --light-bg: #f8f9fa;
            --dark-bg: #1a1a2e;
            --light-text: #f8f9fa;
            --dark-text: #2c3e50;
            --card-light: #ffffff;
            --card-dark: #2d2d44;
            --gradient: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            --success-color: #2ecc71;
            --error-color: #e74c3c;
        }

        body {
            background: var(--gradient);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
        }

        .login-container {
            background-color: var(--card-light);
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            padding: 30px;
            width: 100%;
            max-width: 400px;
            margin: auto;
        }

        .chat-background {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .typing-animation {
            overflow: hidden;
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: 0.15em;
            animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
            color: var(--dark-text);
            border-right: 3px solid var(--primary-color);
        }

        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }

        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--primary-color) }
        }

        .btn-primary {
            background: var(--gradient);
            border: none;
            transition: all 0.3s ease;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .support-btn {
            position: fixed;
            bottom: 20px;
            left: 20px;
            z-index: 1000;
            background: var(--gradient);
            color: white;
            border-radius: 50%;
            width: 60px;
            height: 60px;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .support-btn:hover {
            transform: scale(1.1);
            color: white;
        }

        #main-page {
            display: none;
            width: 100%;
            padding: 20px;
            animation: fadeIn 0.5s ease;
        }

        .main-container {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            max-width: 1000px;
            margin: 0 auto;
        }

        .welcome-header {
            text-align: center;
            margin-bottom: 30px;
            color: var(--dark-text);
        }

        .feature-card {
            border: none;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
            margin-bottom: 20px;
            background: white;
            height: 100%;
        }

        .feature-card:hover {
            transform: translateY(-5px);
        }

        .nav-tabs .nav-link {
            color: var(--dark-text);
        }

        .nav-tabs .nav-link.active {
            background: var(--gradient);
            color: white;
            border: none;
        }

        .alert-box {
            display: none;
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 1050;
            min-width: 300px;
            text-align: center;
            animation: fadeIn 0.5s, fadeOut 0.5s 2.5s forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; top: 0; }
            to { opacity: 1; top: 20px; }
        }

        @keyframes fadeOut {
            from { opacity: 1; top: 20px; }
            to { opacity: 0; top: 0; visibility: hidden; }
        }

        .user-profile {
            display: flex;
            align-items: center;
            justify-content: flex-end;
            margin-bottom: 20px;
            padding: 10px;
            background: rgba(52, 152, 219, 0.1);
            border-radius: 10px;
        }

        .user-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--gradient);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            margin-left: 10px;
        }

        .link-item {
            border-radius: 8px;
            margin-bottom: 15px;
            transition: all 0.3s ease;
            background: white;
        }

        .link-item:hover {
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .copy-btn {
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .copy-btn:hover {
            transform: scale(1.1);
        }

        .premium-badge {
            background: linear-gradient(135deg, #ffce54 0%, #f17e4a 100%);
            color: white;
            padding: 3px 8px;
            border-radius: 4px;
            font-size: 0.8rem;
            margin-right: 5px;
        }

        .search-box {
            position: relative;
            margin-bottom: 20px;
        }

        .search-box i {
            position: absolute;
            top: 12px;
            right: 15px;
            color: #6c757d;
        }

        .search-box input {
            padding-right: 40px;
            border-radius: 25px;
        }

        .category-filter {
            margin-bottom: 20px;
        }

        .category-btn {
            margin-left: 5px;
            margin-bottom: 5px;
            border-radius: 20px;
        }

        .theme-switcher {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
        }

        .dark-mode {
            --light-bg: #1a1a2e;
            --dark-bg: #f8f9fa;
            --light-text: #2c3e50;
            --dark-text: #f8f9fa;
            --card-light: #2d2d44;
            --card-dark: #ffffff;
        }

        .dark-mode body {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
        }

        .dark-mode .login-container,
        .dark-mode .main-container,
        .dark-mode .feature-card,
        .dark-mode .link-item {
            background-color: var(--card-light);
            color: var(--light-text);
        }

        .dark-mode .form-control {
            background-color: #3a3a5a;
            border-color: #4a4a6a;
            color: var(--light-text);
        }

        .dark-mode .form-control:focus {
            background-color: #3a3a5a;
            border-color: var(--primary-color);
            color: var(--light-text);
            box-shadow: 0 0 0 0.25rem rgba(52, 152, 219, 0.25);
        }

        .dark-mode .card {
            background-color: var(--card-light);
            color: var(--light-text);
        }

        .dark-mode .user-profile {
            background: rgba(52, 152, 219, 0.2);
        }

        .loading-spinner {
            display: none;
            text-align: center;
            padding: 20px;
        }

        .spinner-border {
            width: 3rem;
            height: 3rem;
        }
    </style>
</head>
<body class="chat-background">
    <!-- صفحه ورود -->
    <div id="login-page">
        <div class="login-container">
            <div class="text-center mb-4">
                <h3 class="typing-animation">یک دنیای متفاوت از لینک‌ها<br>LINK VIPZEXNET</h3>
            </div>
            <ul class="nav nav-tabs mb-3" id="loginTabs" role="tablist">
                <li class="nav-item" role="presentation">
                    <button class="nav-link active" id="login-tab" data-bs-toggle="tab" data-bs-target="#login" type="button" role="tab">ورود</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="register-tab" data-bs-toggle="tab" data-bs-target="#register" type="button" role="tab">ثبت نام</button>
                </li>
            </ul>
            <div class="tab-content" id="loginTabContent">
                <div class="tab-pane fade show active" id="login" role="tabpanel">
                    <form id="login-form">
                        <div class="mb-3">
                            <label for="login-username" class="form-label">نام کاربری</label>
                            <input type="text" class="form-control" id="login-username" required>
                        </div>
                        <div class="mb-3">
                            <label for="login-password" class="form-label">رمز عبور</label>
                            <input type="password" class="form-control" id="login-password" required>
                        </div>
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="remember-login">
                            <label class="form-check-label" for="remember-login">مرا به خاطر بسپار</label>
                        </div>
                        <button type="submit" class="btn btn-primary w-100">ورود</button>
                    </form>
                </div>
                <div class="tab-pane fade" id="register" role="tabpanel">
                    <form id="register-form">
                        <div class="mb-3">
                            <label for="register-username" class="form-label">نام کاربری</label>
                            <input type="text" class="form-control" id="register-username" required>
                        </div>
                        <div class="mb-3">
                            <label for="register-email" class="form-label">ایمیل</label>
                            <input type="email" class="form-control" id="register-email" required>
                        </div>
                        <div class="mb-3">
                            <label for="register-password" class="form-label">رمز عبور</label>
                            <input type="password" class="form-control" id="register-password" required>
                        </div>
                        <div class="mb-3">
                            <label for="register-confirm-password" class="form-label">تکرار رمز عبور</label>
                            <input type="password" class="form-control" id="register-confirm-password" required>
                        </div>
                        <button type="submit" class="btn btn-primary w-100">ثبت نام</button>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!-- صفحه اصلی (پس از ورود) -->
    <div id="main-page">
        <div class="main-container">
            <div class="user-profile">
                <div class="user-info">
                    <span id="user-fullname">کاربر مهمان</span>
                    <span class="badge bg-primary me-2" id="user-type">حالت معمولی</span>
                </div>
                <div class="user-avatar" id="user-avatar">U</div>
            </div>

            <div class="welcome-header">
                <h2>خوش آمدید به <span class="text-primary">LINK VIPZEXNET</span></h2>
                <p>یک دنیای متفاوت از لینک‌های پریمیوم و ویژه</p>
            </div>

            <div class="search-box">
                <input type="text" class="form-control" id="search-input" placeholder="جستجو در لینک‌ها...">
                <i class="bi bi-search"></i>
            </div>

            <div class="category-filter">
                <button class="btn btn-outline-primary category-btn active" data-category="all">همه</button>
                <button class="btn btn-outline-primary category-btn" data-category="social">شبکه‌های اجتماعی</button>
                <button class="btn btn-outline-primary category-btn" data-category="entertainment">سرگرمی</button>
                <button class="btn btn-outline-primary category-btn" data-category="shopping">خرید</button>
                <button class="btn btn-outline-primary category-btn" data-category="education">آموزشی</button>
            </div>
            
            <div class="loading-spinner" id="loading-spinner">
                <div class="spinner-border text-primary" role="status">
                    <span class="visually-hidden">Loading...</span>
                </div>
            </div>

            <div class="row" id="links-container">
                <!-- لینک‌ها در اینجا نمایش داده می‌شوند -->
            </div>
            
            <div class="text-center mt-4">
                <button id="logout-btn" class="btn btn-outline-primary">خروج از حساب</button>
            </div>
        </div>
    </div>

    <!-- دکمه پشتیبانی -->
    <a href="#" class="support-btn" id="support-button">
        <i class="bi bi-headset" style="font-size: 1.5rem;"></i>
    </a>

    <!-- تغییر تم -->
    <div class="theme-switcher">
        <button class="btn btn-outline-secondary" id="theme-toggle">
            <i class="bi bi-moon"></i>
        </button>
    </div>

    <!-- پیام alert -->
    <div class="alert-box alert alert-success" role="alert" id="success-alert">
        عملیات با موفقیت انجام شد!
    </div>

    <div class="alert-box alert alert-danger" role="alert" id="error-alert">
        خطایی رخ داده است!
    </div>

    <!-- اسکریپت پشتیبانی Goftino -->
    <script type="text/javascript">
        !function(){var i="UN9vJh",a=window,d=document;function g(){var g=d.createElement("script"),s="https://www.goftino.com/widget/"+i,l=localStorage.getItem("goftino_"+i);g.async=!0,g.src=l?s+"?o="+l:s;d.getElementsByTagName("head")[0].appendChild(g);}"complete"===d.readyState?g():a.attachEvent?a.attachEvent("onload",g):a.addEventListener("load",g,!1);}();
    </script>

    <!-- اسکریپت‌های بوتسترپ و منطق برنامه -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // داده‌های نمونه برای لینک‌ها
        const sampleLinks = [
            { id: 1, title: 'فیس‌بوک پریمیوم', url: 'https://facebook.com/premium', category: 'social', isPremium: true, description: 'دسترسی ویژه به فیس‌بوک' },
            { id: 2, title: 'یوتیوب VIP', url: 'https://youtube.com/vip', category: 'social', isPremium: true, description: 'تماشای ویدیو بدون تبلیغات' },
            { id: 3, title: 'اینستاگرام ویژه', url: 'https://instagram.com/special', category: 'social', isPremium: false, description: 'امکانات اضافی اینستاگرام' },
            { id: 4, title: 'نتفلیکس رایگان', url: 'https://netflix.com/free', category: 'entertainment', isPremium: true, description: 'تماشای فیلم و سریال رایگان' },
            { id: 5, title: 'آمازون تخفیف‌دار', url: 'https://amazon.com/discount', category: 'shopping', isPremium: false, description: 'خرید با تخفیف ویژه' },
            { id: 6, title: 'دوره‌های آموزشی ویژه', url: 'https://courses.com/vip', category: 'education', isPremium: true, description: 'دسترسی به دوره‌های آموزشی پریمیوم' },
            { id: 7, title: 'تلگرام طلایی', url: 'https://telegram.org/gold', category: 'social', isPremium: true, description: 'تلگرام با امکانات اضافی' },
            { id: 8, title: 'توییتر ویژه', url: 'https://twitter.com/special', category: 'social', isPremium: false, description: 'توییتر با قابلیت‌های بیشتر' }
        ];

        document.addEventListener('DOMContentLoaded', function() {
            // بررسی وضعیت ذخیره شده ورود
            checkLoginStatus();

            // مدیریت فرم ورود
            document.getElementById('login-form').addEventListener('submit', function(e) {
                e.preventDefault();
                const username = document.getElementById('login-username').value;
                const password = document.getElementById('login-password').value;
                const rememberMe = document.getElementById('remember-login').checked;
                
                // شبیه‌سازی ورود
                simulateLogin(username, password, rememberMe);
            });
            
            // مدیریت فرم ثبت‌نام
            document.getElementById('register-form').addEventListener('submit', function(e) {
                e.preventDefault();
                const username = document.getElementById('register-username').value;
                const email = document.getElementById('register-email').value;
                const password = document.getElementById('register-password').value;
                const confirmPassword = document.getElementById('register-confirm-password').value;
                
                if (password !== confirmPassword) {
                    showAlert('error', 'رمز عبور و تکرار آن مطابقت ندارند');
                    return;
                }
                
                // شبیه‌سازی ثبت‌نام
                simulateRegister(username, email, password);
            });
            
            // مدیریت دکمه خروج
            document.getElementById('logout-btn').addEventListener('click', function() {
                logout();
            });
            
            // مدیریت دکمه پشتیبانی
            document.getElementById('support-button').addEventListener('click', function(e) {
                e.preventDefault();
                openSupport();
            });

            // مدیریت تغییر تم
            document.getElementById('theme-toggle').addEventListener('click', function() {
                toggleTheme();
            });

            // مدیریت جستجو
            document.getElementById('search-input').addEventListener('input', function() {
                filterLinks();
            });

            // مدیریت فیلتر دسته‌بندی
            document.querySelectorAll('.category-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    // حذف کلاس active از همه دکمه‌ها
                    document.querySelectorAll('.category-btn').forEach(b => {
                        b.classList.remove('active');
                    });
                    // اضافه کردن کلاس active به دکمه کلیک شده
                    this.classList.add('active');
                    
                    filterLinks();
                });
            });
        });

        // بررسی وضعیت ورود
        function checkLoginStatus() {
            const savedUser = localStorage.getItem('vipzexnet_user');
            if (savedUser) {
                const user = JSON.parse(savedUser);
                showMainPage(user);
            }
        }

        // شبیه‌سازی ورود
        function simulateLogin(username, password, rememberMe) {
            // نمایش اسپینر loading
            document.getElementById('loading-spinner').style.display = 'block';
            
            // شبیه‌سازی تاخیر برای عملیات ورود
            setTimeout(() => {
                // مخفی کردن اسپینر
                document.getElementById('loading-spinner').style.display = 'none';
                
                // در حالت واقعی، اینجا درخواست به سرور ارسال می‌شود
                if (username && password) {
                    const user = {
                        username: username,
                        email: username + '@example.com',
                        fullname: 'کاربر ' + username,
                        isPremium: username.toLowerCase().includes('vip')
                    };
                    
                    if (rememberMe) {
                        localStorage.setItem('vipzexnet_user', JSON.stringify(user));
                    } else {
                        sessionStorage.setItem('vipzexnet_user', JSON.stringify(user));
                    }
                    
                    showMainPage(user);
                    showAlert('success', 'ورود با موفقیت انجام شد');
                } else {
                    showAlert('error', 'لطفاً نام کاربری و رمز عبور را وارد کنید');
                }
            }, 1500);
        }

        // شبیه‌سازی ثبت‌نام
        function simulateRegister(username, email, password) {
            // نمایش اسپینر loading
            document.getElementById('loading-spinner').style.display = 'block';
            
            // شبیه‌سازی تاخیر برای عملیات ثبت‌نام
            setTimeout(() => {
                // مخفی کردن اسپینر
                document.getElementById('loading-spinner').style.display = 'none';
                
                // در حالت واقعی، اینجا درخواست به سرور ارسال می‌شود
                if (username && email && password) {
                    showAlert('success', 'ثبت‌نام با موفقیت انجام شد. اکنون می‌توانید وارد شوید.');
                    // تغییر به تب ورود
                    document.getElementById('login-tab').click();
                    
                    // پاک کردن فرم ثبت‌نام
                    document.getElementById('register-form').reset();
                } else {
                    showAlert('error', 'لطفاً تمام فیلدها را پر کنید');
                }
            }, 1500);
        }

        // نمایش صفحه اصلی
        function showMainPage(user) {
            document.getElementById('login-page').style.display = 'none';
            document.getElementById('main-page').style.display = 'block';
            
            // به روزرسانی اطلاعات کاربر
            document.getElementById('user-fullname').textContent = user.fullname;
            document.getElementById('user-avatar').textContent = user.username.charAt(0).toUpperCase();
            
            if (user.isPremium) {
                document.getElementById('user-type').textContent = 'حساب پریمیوم';
                document.getElementById('user-type').classList.remove('bg-primary');
                document.getElementById('user-type').classList.add('bg-warning');
            } else {
                document.getElementById('user-type').textContent = 'حساب معمولی';
                document.getElementById('user-type').classList.remove('bg-warning');
                document.getElementById('user-type').classList.add('bg-primary');
            }
            
            // نمایش لینک‌ها
            displayLinks();
        }

        // نمایش لینک‌ها
        function displayLinks() {
            const linksContainer = document.getElementById('links-container');
            linksContainer.innerHTML = '';
            
            sampleLinks.forEach(link => {
                const linkElement = document.createElement('div');
                linkElement.className = 'col-md-6';
                linkElement.innerHTML = `
                    <div class="link-item card">
                        <div class="card-body">
                            <h5 class="card-title">
                                ${link.isPremium ? '<span class="premium-badge">پریمیوم</span>' : ''}
                                ${link.title}
                            </h5>
                            <p class="card-text">${link.description}</p>
                            <div class="d-flex justify-content-between align-items-center">
                                <span class="badge bg-secondary">${getCategoryName(link.category)}</span>
                                <div>
                                    <a href="${link.url}" target="_blank" class="btn btn-sm btn-primary">باز کردن</a>
                                    <button class="btn btn-sm btn-outline-secondary copy-btn" data-url="${link.url}">
                                        <i class="bi bi-clipboard"></i>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                `;
                linksContainer.appendChild(linkElement);
            });
            
            // اضافه کردن event listener برای دکمه‌های کپی
            document.querySelectorAll('.copy-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const url = this.getAttribute('data-url');
                    copyToClipboard(url);
                });
            });
        }

        // فیلتر کردن لینک‌ها بر اساس جستجو و دسته‌بندی
        function filterLinks() {
            const searchText = document.getElementById('search-input').value.toLowerCase();
            const activeCategory = document.querySelector('.category-btn.active').getAttribute('data-category');
            
            const linksContainer = document.getElementById('links-container');
            linksContainer.innerHTML = '';
            
            const filteredLinks = sampleLinks.filter(link => {
                const matchesSearch = link.title.toLowerCase().includes(searchText) || 
                                    link.description.toLowerCase().includes(searchText);
                const matchesCategory = activeCategory === 'all' || link.category === activeCategory;
                
                return matchesSearch && matchesCategory;
            });
            
            if (filteredLinks.length === 0) {
                linksContainer.innerHTML = `
                    <div class="col-12 text-center py-5">
                        <i class="bi bi-search" style="font-size: 3rem;"></i>
                        <h4 class="mt-3">هیچ لینکی یافت نشد</h4>
                        <p>لطفاً عبارت جستجو یا دسته‌بندی را تغییر دهید</p>
                    </div>
                `;
                return;
            }
            
            filteredLinks.forEach(link => {
                const linkElement = document.createElement('div');
                linkElement.className = 'col-md-6';
                linkElement.innerHTML = `
                    <div class="link-item card">
                        <div class="card-body">
                            <h5 class="card-title">
                                ${link.isPremium ? '<span class="premium-badge">پریمیوم</span>' : ''}
                                ${link.title}
                            </h5>
                            <p class="card-text">${link.description}</p>
                            <div class="d-flex justify-content-between align-items-center">
                                <span class="badge bg-secondary">${getCategoryName(link.category)}</span>
                                <div>
                                    <a href="${link.url}" target="_blank" class="btn btn-sm btn-primary">باز کردن</a>
                                    <button class="btn btn-sm btn-outline-secondary copy-btn" data-url="${link.url}">
                                        <i class="bi bi-clipboard"></i>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                `;
                linksContainer.appendChild(linkElement);
            });
            
            // اضافه کردن event listener برای دکمه‌های کپی
            document.querySelectorAll('.copy-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const url = this.getAttribute('data-url');
                    copyToClipboard(url);
                });
            });
        }

        // دریافت نام فارسی دسته‌بندی
        function getCategoryName(category) {
            const categories = {
                'social': 'شبکه اجتماعی',
                'entertainment': 'سرگرمی',
                'shopping': 'خرید',
                'education': 'آموزشی'
            };
            
            return categories[category] || category;
        }

        // کپی کردن به کلیپ‌بورد
        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(() => {
                showAlert('success', 'لینک با موفقیت کپی شد');
            }).catch(err => {
                showAlert('error', 'خطا در کپی کردن لینک');
            });
        }

        // نمایش alert
        function showAlert(type, message) {
            const alert = document.getElementById(type + '-alert');
            alert.querySelector('.alert-message')?.remove();
            
            const messageElement = document.createElement('div');
            messageElement.className = 'alert-message';
            messageElement.textContent = message;
            alert.appendChild(messageElement);
            
            alert.style.display = 'block';
            alert.style.animation = 'none';
            void alert.offsetHeight; // Trigger reflow
            alert.style.animation = null;
            
            setTimeout(() => {
                alert.style.display = 'none';
            }, 3000);
        }

        // باز کردن پشتیبانی
        function openSupport() {
            if (typeof Goftino !== 'undefined') {
                Goftino.open();
            } else {
                showAlert('error', 'سیستم پشتیبانی در حال حاضر در دسترس نیست. لطفاً稍后再试。');
            }
        }

        // تغییر تم
        function toggleTheme() {
            document.body.classList.toggle('dark-mode');
            const themeToggle = document.getElementById('theme-toggle');
            const icon = themeToggle.querySelector('i');
            
            if (document.body.classList.contains('dark-mode')) {
                icon.classList.remove('bi-moon');
                icon.classList.add('bi-sun');
                localStorage.setItem('vipzexnet_theme', 'dark');
            } else {
                icon.classList.remove('bi-sun');
                icon.classList.add('bi-moon');
                localStorage.setItem('vipzexnet_theme', 'light');
            }
        }

        // خروج از حساب
        function logout() {
            localStorage.removeItem('vipzexnet_user');
            sessionStorage.removeItem('vipzexnet_user');
            
            document.getElementById('main-page').style.display = 'none';
            document.getElementById('login-page').style.display = 'flex';
            
            // پاک کردن فرم‌ها
            document.getElementById('login-form').reset();
            document.getElementById('register-form').reset();
            
            showAlert('success', 'خروج با موفقیت انجام شد');
        }

        // بررسی تم ذخیره شده
        window.addEventListener('load', function() {
            const savedTheme = localStorage.getItem('vipzexnet_theme');
            if (savedTheme === 'dark') {
                document.body.classList.add('dark-mode');
                const themeToggle = document.getElementById('theme-toggle');
                const icon = themeToggle.querySelector('i');
                icon.classList.remove('bi-moon');
                icon.classList.add('bi-sun');
            }
        });
    </script>
</body>
</html>
