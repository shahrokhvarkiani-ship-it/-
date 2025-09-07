# -<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ثبت اطلاعات سمینار</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c 0%, #b21f1f 50%, #fdbb2d 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }
        
        .container {
            width: 100%;
            max-width: 500px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 15px 50px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(to right, #1a2a6c, #b21f1f);
            color: white;
            padding: 25px;
            text-align: center;
            position: relative;
        }
        
        .header h1 {
            font-size: 24px;
            margin-bottom: 10px;
        }
        
        .header p {
            font-size: 14px;
            opacity: 0.9;
        }
        
        .header::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100%;
            height: 20px;
            background: linear-gradient(135deg, transparent 0%, transparent 50%, white 50%, white 100%);
            background-size: 20px 20px;
        }
        
        .form-container {
            padding: 25px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #444;
        }
        
        input, select {
            width: 100%;
            padding: 14px;
            border: 2px solid #e1e1e1;
            border-radius: 10px;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        input:focus, select:focus {
            border-color: #1a2a6c;
            box-shadow: 0 0 0 3px rgba(26, 42, 108, 0.2);
            outline: none;
        }
        
        .input-with-icon {
            position: relative;
        }
        
        .input-with-icon i {
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            color: #777;
        }
        
        .input-with-icon input {
            padding-left: 45px;
        }
        
        .qr-section {
            text-align: center;
            margin: 20px 0;
            padding: 15px;
            background: #f9f9f9;
            border-radius: 10px;
            border: 2px dashed #ddd;
        }
        
        .qr-code {
            width: 150px;
            height: 150px;
            margin: 0 auto;
            background: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid #eee;
        }
        
        .qr-code span {
            font-size: 12px;
            color: #777;
        }
        
        .checkbox-group {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .checkbox-group input {
            width: auto;
            margin-left: 10px;
        }
        
        .btn-submit {
            background: linear-gradient(to right, #1a2a6c, #b21f1f);
            color: white;
            padding: 16px;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            width: 100%;
            transition: all 0.3s ease;
            margin-top: 10px;
        }
        
        .btn-submit:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .required::after {
            content: " *";
            color: #e74c3c;
        }
        
        .thank-you {
            text-align: center;
            padding: 30px;
            display: none;
        }
        
        .thank-you i {
            font-size: 60px;
            color: #0ac282;
            margin-bottom: 20px;
        }
        
        .thank-you h2 {
            color: #1a2a6c;
            margin-bottom: 15px;
        }
        
        .badge {
            display: inline-block;
            background: linear-gradient(to right, #1a2a6c, #b21f1f);
            color: white;
            padding: 8px 15px;
            border-radius: 50px;
            font-size: 14px;
            margin: 10px 0;
            font-weight: 600;
        }
        
        @media (max-width: 768px) {
            .container {
                border-radius: 15px;
            }
            
            .header {
                padding: 20px;
            }
            
            .form-container {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>سمینار تکنولوژی های نوین</h1>
            <p>لطفا اطلاعات خود را برای دریافت مطالب سمینار وارد کنید</p>
        </div>
        
        <div class="form-container">
            <form id="seminarForm">
                <div class="form-group">
                    <label for="fullname" class="required">نام کامل</label>
                    <div class="input-with-icon">
                        <i class="fas fa-user"></i>
                        <input type="text" id="fullname" placeholder="نام و نام خانوادگی">
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="phone" class="required">شماره تماس</label>
                    <div class="input-with-icon">
                        <i class="fas fa-phone"></i>
                        <input type="tel" id="phone" placeholder="۰۹۱۲XXX۳۴۵۶">
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="email" class="required">ایمیل</label>
                    <div class="input-with-icon">
                        <i class="fas fa-envelope"></i>
                        <input type="email" id="email" placeholder="example@site.com">
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="company">شرکت/سازمان</label>
                    <input type="text" id="company" placeholder="نام شرکت یا سازمان">
                </div>
                
                <div class="form-group">
                    <label for="position">سمت سازمانی</label>
                    <select id="position">
                        <option value="">-- انتخاب کنید --</option>
                        <option value="manager">مدیر</option>
                        <option value="engineer">مهندس</option>
                        <option value="analyst">تحلیلگر</option>
                        <option value="consultant">مشاور</option>
                        <option value="other">سایر</option>
                    </select>
                </div>
                
                <div class="qr-section">
                    <p>برای دریافت مطالب سمینار، QR Code را اسکن کنید</p>
                    <div class="qr-code">
                        <span>QR Code در اینجا نمایش داده می‌شود</span>
                    </div>
                    <div class="badge">
                        <i class="fas fa-download"></i> دریافت مطالب
                    </div>
                </div>
                
                <div class="form-group">
                    <div class="checkbox-group">
                        <input type="checkbox" id="materialRequest" checked>
                        <label for="materialRequest">مایل به دریافت مطالب سمینار هستم</label>
                    </div>
                </div>
                
                <div class="form-group">
                    <div class="checkbox-group">
                        <input type="checkbox" id="futureEvents">
                        <label for="futureEvents">مایل به دریافت invitations رویدادهای آینده هستم</label>
                    </div>
                </div>
                
                <button type="submit" class="btn-submit">
                    <i class="fas fa-paper-plane"></i> ثبت اطلاعات و دریافت مطالب
                </button>
            </form>
            
            <div class="thank-you" id="thankYou">
                <i class="fas fa-check-circle"></i>
                <h2>اطلاعات شما با موفقیت ثبت شد!</h2>
                <p>مطالب سمینار به ایمیل شما ارسال گردید.</p>
                <div class="badge">
                    <i class="fas fa-user-check"></i> شرکت‌کننده سمینار
                </div>
                <p>از حضور شما سپاسگزاریم.</p>
            </div>
        </div>
    </div>

    <script>
        document.getElementById('seminarForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // اعتبارسنجی ساده
            const name = document.getElementById('fullname').value;
            const phone = document.getElementById('phone').value;
            const email = document.getElementById('email').value;
            
            if (!name || !phone || !email) {
                alert('لطفا فیلدهای ضروری را پر کنید');
                return;
            }
            
            // در اینجا می‌توانید اطلاعات را به سرور ارسال کنید
            
            // نمایش پیام تشکر
            document.getElementById('seminarForm').style.display = 'none';
            document.getElementById('thankYou').style.display = 'block';
            
            // شبیه‌سازی ارسال ایمیل (در واقعیت این کار در سرور انجام می‌شود)
            console.log('ایمیل حاوی مطالب سمینار برای کاربر ارسال شد.');
        });
    </script>
</body>
</html>
