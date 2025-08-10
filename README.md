<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Online Service Center</title>
<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    body {
        font-family: 'Segoe UI', sans-serif;
        background-color: #f4f8fb;
        color: #333;
        scroll-behavior: smooth;
    }
    header {
        background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
                    url('https://images.unsplash.com/photo-1521791136064-7986c2920216?auto=format&fit=crop&w=1350&q=80');
        background-size: cover;
        background-position: center;
        color: white;
        text-align: center;
        padding: 50px 20px;
        animation: fadeIn 1.5s ease-in-out;
    }
    header h1 {
        font-size: 38px;
        margin-bottom: 10px;
        text-shadow: 2px 2px 5px rgba(0,0,0,0.4);
    }
    header p {
        font-size: 18px;
        opacity: 0.9;
        text-shadow: 1px 1px 4px rgba(0,0,0,0.4);
    }
    nav {
        background: #023e8a;
        display: flex;
        justify-content: center;
        position: sticky;
        top: 0;
        z-index: 1000;
    }
    nav a {
        color: white;
        padding: 14px 20px;
        text-decoration: none;
        font-weight: bold;
        transition: 0.3s;
    }
    nav a:hover {
        background: #0077b6;
        border-radius: 5px;
        transform: scale(1.05);
    }
    .container {
        max-width: 1100px;
        margin: auto;
        padding: 20px;
    }
    h2 {
        text-align: center;
        color: #023e8a;
        margin: 20px 0;
    }
    .services {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
    }
    .service-category {
        background: white;
        padding: 20px;
        border-radius: 8px;
        box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        transition: 0.3s;
        animation: slideUp 0.8s ease-in-out;
    }
    .service-category:hover {
        transform: translateY(-5px);
        box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }
    .service-category h3 {
        color: #0077b6;
        border-left: 5px solid #0096c7;
        padding-left: 10px;
        margin-bottom: 10px;
    }
    ul {
        list-style: none;
        padding: 0;
    }
    ul li {
        padding: 6px 0;
        font-size: 15px;
        display: flex;
        align-items: center;
    }
    ul li::before {
        content: "✔";
        color: #0096c7;
        margin-right: 8px;
        font-weight: bold;
    }
    /* Why Choose Us */
    .why-choose {
        background: #e0f7fa;
        padding: 20px;
        margin: 30px 0;
        border-radius: 8px;
        text-align: center;
        animation: fadeIn 1s ease-in-out;
    }
    .why-choose h2 {
        margin-bottom: 10px;
    }
    .why-choose p {
        max-width: 800px;
        margin: auto;
        font-size: 16px;
        line-height: 1.6;
    }
    /* Contact Form (Updated) */
    .contact-form {
        background: linear-gradient(135deg, #ffffff, #f0f9ff);
        padding: 15px;
        border-radius: 10px;
        box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        max-width: 400px;
        margin: 20px auto;
        text-align: center;
        animation: fadeIn 1.2s ease-in-out;
    }
    .contact-form h2 {
        font-size: 20px;
        margin-bottom: 8px;
        color: #0077b6;
    }
    .contact-form input,
    .contact-form textarea {
        border: 1px solid #ddd;
        background: #fafafa;
        border-radius: 6px;
        padding: 8px;
        font-size: 14px;
        margin: 5px 0;
        transition: 0.3s;
        width: 100%;
    }
    .contact-form input:focus,
    .contact-form textarea:focus {
        border-color: #0096c7;
        background: #fff;
        outline: none;
        box-shadow: 0 0 5px rgba(0,150,199,0.2);
    }
    .contact-form button {
        background: linear-gradient(90deg, #0096c7, #0077b6);
        color: white;
        padding: 8px 15px;
        border: none;
        border-radius: 6px;
        cursor: pointer;
        font-size: 14px;
        transition: 0.3s;
        width: 100%;
    }
    .contact-form button:hover {
        background: linear-gradient(90deg, #0077b6, #023e8a);
        transform: scale(1.05);
    }
    footer {
        background: #023e8a;
        color: white;
        text-align: center;
        padding: 15px;
        margin-top: 20px;
        font-size: 14px;
    }
    .social-icons a {
        color: white;
        margin: 0 8px;
        text-decoration: none;
        font-size: 18px;
        transition: 0.3s;
    }
    .social-icons a:hover {
        color: #00b4d8;
    }
    /* WhatsApp Button */
    .whatsapp-btn {
        position: fixed;
        bottom: 20px;
        right: 20px;
        background: #25D366;
        color: white;
        padding: 12px 15px;
        border-radius: 50%;
        font-size: 24px;
        text-decoration: none;
        box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }
    /* Animations */
    @keyframes fadeIn {
        from {opacity: 0;}
        to {opacity: 1;}
    }
    @keyframes slideUp {
        from {transform: translateY(20px); opacity: 0;}
        to {transform: translateY(0); opacity: 1;}
    }
</style>
</head>
<body>

<header>
    <h1>Online Service Center</h1>
    <p>All Government, Education & Online Services in One Place</p>
</header>

<nav>
    <a href="#services">Services</a>
    <a href="#why">Why Choose Us</a>
    <a href="#contact">Contact</a>
</nav>

<div class="container" id="services">
    <h2>Our Services</h2>
    <div class="services">
        <div class="service-category">
            <h3>📋 Application & Forms</h3>
            <ul>
                <li>College Admission Form</li>
                <li>IGNOU University Admission</li>
                <li>Government Job Applications</li>
                <li>Bank Job Form</li>
            </ul>
        </div>
        <div class="service-category">
            <h3>🆔 ID & Document Services</h3>
            <ul>
                <li>PAN Card (New / Correction)</li>
                <li>Aadhaar Card Update</li>
                <li>Voter ID Card</li>
                <li>Himcare / e-Shram Card</li>
            </ul>
        </div>
        <div class="service-category">
            <h3>📜 Certificates</h3>
            <ul>
                <li>Bonafide Certificate</li>
                <li>Character Certificate</li>
                <li>Income Certificate</li>
                <li>EWS / Caste Certificate</li>
            </ul>
        </div>
        <div class="service-category">
            <h3>💡 Bill Payments</h3>
            <ul>
                <li>Water Bill</li>
                <li>Electricity Bill</li>
                <li>Garbage Bill</li>
                <li>Property Tax</li>
            </ul>
        </div>
        <div class="service-category">
            <h3>💻 Digital Work</h3>
            <ul>
                <li>English & Hindi Typing</li>
                <li>Word Document Editing</li>
                <li>Excel Sheet Work</li>
                <li>PPT Presentation</li>
            </ul>
        </div>
    </div>
</div>

<div class="why-choose" id="why">
    <h2>Why Choose Us?</h2>
    <p>✅ Fast & Reliable Services | ✅ Affordable Charges | ✅ All Government & Educational Services at One Place | ✅ 100% Customer Satisfaction</p>
</div>

<!-- Updated Contact Form -->
<div class="contact-form" id="contact">
    <h2>📩 Get in Touch</h2>
    <form>
        <input type="text" placeholder="👤 Name" required>
        <input type="email" placeholder="✉ Email" required>
        <textarea placeholder="💬 Message" rows="2" required></textarea>
        <button type="submit">📨 Send</button>
    </form>
</div>

<footer>
    <p>📞 Phone: 7018135514</p>
    <div class="social-icons">
        <a href="#">🌐</a>
        <a href="#">📘</a>
        <a href="#">📷</a>
    </div>
    <p>© 2025 Online Service Center</p>
</footer>

<a href="https://wa.me/917018135514" class="whatsapp-btn">💬</a>

</body>
</html>
