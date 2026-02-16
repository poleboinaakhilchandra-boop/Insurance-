<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>InsureWealth - Insurance for Wealth Building</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Arial', sans-serif; line-height: 1.6; color: #333; }
        header { background: linear-gradient(135deg, #1e3c72, #2a5298); color: white; padding: 1rem 0; position: fixed; width: 100%; top: 0; z-index: 1000; }
        nav ul { list-style: none; display: flex; justify-content: center; }
        nav li { margin: 0 1rem; }
        nav a { color: white; text-decoration: none; font-weight: bold; }
        section { padding: 80px 5%; min-height: 100vh; }
        #hero { background: #f4f4f4; text-align: center; display: flex; flex-direction: column; justify-content: center; align-items: center; }
        h1 { font-size: 3rem; margin-bottom: 1rem; }
        .btn { background: #ff6b35; color: white; padding: 1rem 2rem; text-decoration: none; border-radius: 5px; margin-top: 1rem; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; }
        .card { background: white; padding: 2rem; border-radius: 10px; box-shadow: 0 5px 15px rgba(0,0,0,0.1); }
        #wealth-calc { max-width: 400px; margin: 2rem auto; }
        input { width: 100%; padding: 0.5rem; margin: 0.5rem 0; border: 1px solid #ddd; border-radius: 5px; }
        #result { font-size: 1.5rem; font-weight: bold; color: #ff6b35; }
        footer { background: #333; color: white; text-align: center; padding: 2rem; }
        @media (max-width: 768px) { h1 { font-size: 2rem; } nav ul { flex-direction: column; } }
    </style>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#topics">Topics</a></li>
                <li><a href="#calculator">Calculator</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero">
        <h1>Build Wealth Through Smart Insurance</h1>
        <p>Explore how insurance protects assets while fueling long-term growth, financial planning, and wealth creation.[web:10][web:14]</p>
        <a href="#topics" class="btn">Learn More</a>
    </section>

    <section id="topics">
        <h2>Key Topics</h2>
        <div class="grid">
            <div class="card">
                <h3>Wealth Building</h3>
                <p>Whole life and ULIP policies build cash value over time, offering tax-deferred growth alongside protection.[web:9][web:13]</p>
            </div>
            <div class="card">
                <h3>Wealth Creation</h3>
                <p>Integrate insurance with investments to create legacy wealth, using permanent policies for liquidity and asset transfer.[web:10][web:17]</p>
            </div>
            <div class="card">
                <h3>Financial Planning</h3>
                <p>Assess needs with advisors; combine health, life, and property insurance for comprehensive risk management.[web:9][web:12]</p>
            </div>
            <div class="card">
                <h3>Long-Term Growth</h3>
                <p>Long-term care and disability insurance preserve wealth from medical costs, ensuring investments compound undisturbed.[web:10][web:14]</p>
        </div>
    </section>

    <section id="calculator">
        <h2>Simple Wealth Projection Tool</h2>
        <p>Test how annual insurance savings contribute to long-term growth (assumes 7% avg return).</p>
        <div id="wealth-calc">
            <input type="number" id="annualSave" placeholder="Annual Insurance Savings (₹)" value="50000">
            <input type="number" id="years" placeholder="Years" value="20">
            <button onclick="calculate()">Calculate Future Value</button>
            <div id="result"></div>
        </div>
    </section>

    <section id="contact">
        <h2>Get Started</h2>
        <p>Ready for personalized financial planning? Contact us for a free consultation on insurance-driven wealth strategies.[web:11][web:12]</p>
        <form style="max-width: 500px; margin: 2rem auto;">
            <input type="email" placeholder="Your Email" required>
            <button type="submit" class="btn">Request Quote</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2026 InsureWealth. All rights reserved. | Built with HTML/CSS/JS for aspiring developers.[cite:3]</p>
    </footer>

    <script>
        function calculate() {
            const annual = parseFloat(document.getElementById('annualSave').value);
            const years = parseInt(document.getElementById('years').value);
            const rate = 0.07; // 7% annual growth
            const futureValue = annual * ((Math.pow(1 + rate, years) - 1) / rate);
            document.getElementById('result').textContent = `Projected Wealth: ₹${futureValue.toLocaleString('en-IN', {maximumFractionDigits: 0})}`;
        }

        // Smooth scroll for nav links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
            });
        });
    </script>
</body>
</html>
