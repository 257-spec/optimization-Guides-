<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Optimizer Hub | Health & Hormones</title>
    <style>
        :root {
            --primary: #4e7d48;
            --accent: #81b37a;
            --bg: #121212;
            --card-bg: #1e1e1e;
            --text: #ffffff;
            --sub-text: #b2bec3;
        }
        
        * { box-sizing: border-box; }
        body { 
            font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto; 
            background-color: var(--bg); 
            color: var(--text); 
            margin: 0; 
            display: flex; 
            flex-direction: column; 
            align-items: center; 
            padding: 20px;
            line-height: 1.6;
            position: relative;
            min-height: 100vh;
        }

        /* === PYRAMID BACKGROUND === */
        body::before {
            content: "";
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 90%;
            max-width: 700px;
            height: 90%;
            max-height: 700px;
            z-index: 0;
            opacity: 0.08;
            pointer-events: none;
            background: radial-gradient(ellipse at center, transparent 30%, rgba(78, 125, 72, 0.05) 70%);
        }

        .pyramid-bg {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 0;
            opacity: 0.10;
            font-family: 'Courier New', monospace;
            text-align: center;
            line-height: 1.7;
            color: #81b37a;
            font-size: clamp(10px, 1.8vw, 18px);
            white-space: pre;
            pointer-events: none;
            user-select: none;
            letter-spacing: 0.5px;
            text-shadow: 0 0 30px rgba(78, 125, 72, 0.15);
            width: 100%;
        }

        /* Keep content above background */
        .header, .container, .cta-box, .footer {
            position: relative;
            z-index: 1;
        }

        .header { text-align: center; margin: 30px 0; max-width: 400px; }
        .header h1 { font-size: 1.8rem; margin-bottom: 8px; color: var(--primary); letter-spacing: -0.5px; }
        .header p { font-size: 1rem; color: var(--sub-text); margin: 0; }

        .container { width: 100%; max-width: 420px; }

        .guide-card {
            background: var(--card-bg);
            border: 1px solid #333;
            border-radius: 16px;
            padding: 18px;
            margin-bottom: 12px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.3);
            transition: all 0.2s ease;
            backdrop-filter: blur(2px);
            background: rgba(30, 30, 30, 0.92);
        }
        .guide-card:active { transform: scale(0.98); background: #252525; }
        .guide-card span:first-child { font-weight: 600; font-size: 1.05rem; }

        .guide-content {
            display: none;
            background: rgba(30, 30, 30, 0.95);
            margin: -10px 5px 15px 5px;
            padding: 20px;
            border-bottom-left-radius: 16px;
            border-bottom-right-radius: 16px;
            border: 1px solid #333;
            border-top: none;
            animation: fadeIn 0.3s ease;
            backdrop-filter: blur(4px);
            position: relative;
            z-index: 2;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-5px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .guide-text { font-size: 0.95rem; color: #e0e0e0; white-space: pre-line; }

        .cta-box {
            margin-top: 40px;
            padding: 25px;
            background: var(--primary);
            color: white;
            border-radius: 20px;
            text-align: center;
            width: 100%;
            position: relative;
            z-index: 1;
        }
        .cta-box h3 { margin-top: 0; font-size: 1.3rem; }
        .cta-link {
            display: inline-block;
            background: white;
            color: #1a4314;
            padding: 14px 28px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 15px;
        }

        .footer { margin: 40px 0; font-size: 0.8rem; color: #636e72; text-align: center; position: relative; z-index: 1; }
    </style>
</head>
<body>

    <!-- ===== PYRAMID BACKGROUND (ASCII) ===== -->
    <div class="pyramid-bg">
                    ┌─────────────────────┐
                    │     ENDOCRINOLOGY    │
                    │   (Hormonal Master)  │
                    │ ┌─────────────────┐  │
                    │ │   NUTRITION     │  │
                    │ │ (Metabolic Fuel)│  │
                    │ │ ┌─────────────┐ │  │
                    │ │ │ SOMNOLOGY   │ │  │
                    │ │ │(Restorative)│ │  │
                    │ │ └─────────────┘ │  │
                    │ └─────────────────┘  │
                    └─────────────────────┘
    </div>

    <div class="header">
        <h1>Optimizer Hub 🌿</h1>
        <p>Expert protocols for your health journey</p>
    </div>

    <div class="container">

        <div class="guide-card" onclick="toggleGuide('guide1')">
            <span>🥗 Nutrition Fundamentals</span>
            <span>↓</span>
        </div>
        <div id="guide1" class="guide-content">
            <p class="guide-text">
                <strong>Key Targets:</strong>
                • Focus on whole-food fats for hormone synthesis.
                • Include fermented foods (Kefir/Sauerkraut).
                • Eliminate seed oils and processed sugars.
                • have a macro based balanced diet focus on micros enough nutrients 
                • include in root vegetables, fruits meat organs raw dairy animal fats only for cooking 
                • time your foods focus on quality
            </p> 
        </div>

        <div class="guide-card" onclick="toggleGuide('guide2')">
            <span>💤 Sleep & Recovery</span>
            <span>↓</span>
        </div>
        <div id="guide2" class="guide-content">
            <p class="guide-text">
                <strong>Optimization:</strong>
                • Room temp below 68°F (20°C).
                • Magnesium Glycinate 30-60 mins before bed.
                • No blue light 1-2 hours before sleep.
                • avoid light for the last 2 hours at most have a dim warm toned lamp
                • do some journaling/reading and stretching 
                • consider in glycine 3-5g for better sleep quality
            </p> 
        </div>

        <div class="guide-card" onclick="toggleGuide('guide3')">
            <span>📏 Height Optimization</span>
            <span>↓</span>
        </div>
        <div id="guide3" class="guide-content">
            <p class="guide-text">
                <strong>Protocol:</strong>
                • heavy compounds, explosive movements HIIT Sprints 
                • nutrient dense foods collagen and vit C getting your micronutrients in
                • zinc Mg k2 phosphorus calcium vit D boron b Vitamins 
                • getting carbs in around workouts, getting enough leucine- whey dairy meat
                • a lot of raw dairy cheese, colostrum milk kefir Quark etc
                • enough macros generally 1g of each per lb of bw more if your physical demands it 
                • optimizing sleep to absolute maximum capacity 
                • optimizing other hormones testosterone DHT balancing estrogen thyroid hormones
                • prolactin cortisol
            </p>
        </div>
        
        <div class="guide-card" onclick="toggleGuide('guide4')">
            <span>🦴 Bone Mass</span>
            <span>↓</span>
        </div>
        <div id="guide4" class="guide-content">
            <p class="guide-text">
                <strong>Protocol:</strong>
                • optimizing hormones like GH igf1 testosterone DHT estrogen thyroid hormones etc
                • focusing on sleep, diet micronutrient rich foods like liver old raw cheese oysters meat
                • getting a lot of macros in 1g of each per lb of bw
                • sprints heavy lifts explosive movements 
                • raw dairy ofc
                • a bone growth formula-Raw Beetroot Juice (Wait 30 mins)
                • Explosive Movements (Jumps/Sprints)y + Whey Shake
                • Sweet or Regular Potatoes
             seconds)
            </p>
        </div>
            
        <div class="guide-card" onclick="toggleGuide('guide5')">
            <span>💊 Supplement Timing</span>
            <span>↓</span>
        </div>
        <div id="guide5" class="guide-content">
            <p class="guide-text">
                <strong>Timing & Pairing:</strong>
                • vitamin D, morning with fats K2 calcium and boron
                • and b vitamins, for midday omega 3s- fats and iron and collagen, pair with vitamin C
                • at night magnesium, glycine L citrulline/L arginine 
                • zinc (not before bed or close to magnesium)
                • fat soluble vitamins A,D,E,K -pair with fats 
                • keep out magnesium iron calcium zinc away from each other by 3-4 hours 
                • always pair iron and collagen with vitamin C
                • make sure to get copper along with zinc as they deplete each other
            </p>
        </div>

        <div class="guide-card" onclick="toggleGuide('guide6')">
            <span>📈 GH-IGF1 Optimization</span>
            <span>↓</span>
        </div>
        <div id="guide6" class="guide-content">
            <p class="guide-text">
                <strong>conclude in</strong> 
                sleep 
                excersice 
                protein and carb focused diet
                enough micronutrients and macros
                nutrient dense foods
                raw dairy 
                plyometrics 
                L citrulline Alpha gpc l arginine before bed
                optimizing dopamine levels via being in nature less on phone and optimize testosterone and DHT levels 
                and lastly balancing other hormones such as estrogen/estradiol t3,4 prolactin Cortisol
            </p>
        </div>

        <div class="guide-card" onclick="toggleGuide('guide7')">
            <span>🔥 Testosterone & DHT</span>
            <span>↓</span>
        </div>
        <div id="guide7" class="guide-content">
            <p class="guide-text">
                <strong>conclude in</strong>
                high quality sleep
                heavy compounds and explosive movements 
                high fat/cholesterol focused diet 
                micros -
                boron
                mG
                zinc
                vitD
                L carnitine tartrate 
                B Vitamins 1-12
                be in the sun 24/7
                avoid fapping and watching porn
                manage your Cortisol and prolactin levels 
                adapt a masculine and confident mindset and behavior
            </p>
        </div>

        <div class="guide-card" onclick="toggleGuide('guide8')">
            <span>🧬 Lowering Aromatase-E2</span>
            <span>↓</span>
        </div>
        <div id="guide8" class="guide-content">
            <p class="guide-text">
                <strong>Protocol:</strong>
                15-30mg Zinc Balanced with 1-2mg copper 
                5-10 thousand UI vitamin D3
                400mg magnesium, malate or glycinate 
                Raw carrots 
                Fiber intake 
                Coffee/caffeine 150-200mg unless sensitive 
                Low dose nicotine pills (highly addictive, beware)
                Losing fat
                Increasing DHT and supporting 5AR 
                Avoid soy, flaxseeds DHT blockers, endocrine disruptors
                Manage cortisol, 
                Maintain regular exercise 
                Steamed cruciferous vegs or DIM supplement 
                avoid conventional dairy
            </p>
        </div>

        <div class="guide-card" onclick="toggleGuide('guide9')">
            <span>🧬 Lowering SHBG</span>
            <span>↓</span>
        </div>
        <div id="guide9" class="guide-content">
            <p class="guide-text">
                <strong>conclude in</strong>
                stress Management 
                high macro based diet (high protein fats carbs 1-1.5g of each per lb of bw)
                micronutrients
                boron
                magnesium 
                zinc 
                vit D
                and crucial one, taking care of your liver health 
                consider in cooked cruciferous vegetables few times per week
            </p>
        </div>

        <div class="guide-card" onclick="toggleGuide('guide10')">
            <span>📉 Cortisol & Prolactin</span>
            <span>↓</span>
        </div>
        <div id="guide10" class="guide-content">
            <p class="guide-text">
                <strong>conclude in</strong>
                synchronizing circadian rhythm high quality 8-10 hrs sleep
                vit b6 p5p version 
                vit C 
                zinc
                Mg
                being in nature 
                cold exposure here and there
                excericising 
                less time on phone 
                no fapping or watching porn
                additionally conclude in L theanine before bed/in the evening
            </p>
        </div>

        <div class="guide-card" onclick="toggleGuide('guide11')">
            <span>🦋 Thyroid Optimization</span>
            <span>↓</span>
        </div>
        <div id="guide11" class="guide-content">
            <p class="guide-text">
                <strong>conclude in</strong> 
                focusing on sleep
                optimal serotonin levels (watching sunset and sunrise, dark chocolate chicken greek yogurt eggs)
                keeping Cortisol low
                optimal carb and protein intake
                micros 
                iodine 
                tyrosine 
                vit A
                vit D
                Mg
                zinc
                iron
                selenium
            </p>
        </div>
         
        <div class="cta-box">
            <h3>Ready for 1-on-1 Coaching?</h3>
            <p>I'll help you build a personalized protocol.</p>
            <a href="https://www.tiktok.com/@mid_tier_endocrinologist?_r=1&_t=ZN-94g4p2BUi4k" class="cta-link">Send me a message</a>
        </div>
    </div>

    <div class="footer">© 2026 Optimization Protocol</div>

    <script>
        function toggleGuide(id) {
            const element = document.getElementById(id);
            if (!element) return;
            
            const isVisible = element.style.display === 'block';
            
            document.querySelectorAll('.guide-content').forEach(el => {
                el.style.display = 'none';
            });
            
            element.style.display = isVisible ? 'none' : 'block';
        }
    </script>

</body>
</html>
