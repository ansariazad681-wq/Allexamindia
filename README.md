<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <meta name="description" content="ALL EXAM INDIA - विभिन्न कैटेगरी में हिंदी प्रश्न, दैनिक करंट अफेयर्स और MCQ प्रैक्टिस।"/>
    <meta name="keywords" content="ALL EXAM INDIA, हिंदी प्रश्न, करंट अफेयर्स, MCQ, क्विज"/>
    <title>ALL EXAM INDIA - Quiz Portal</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet"/>
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"/>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', sans-serif;
        }

        body {
            background-color: #f0f4f8;
            color: #333;
            line-height: 1.6;
        }

        header {
            background: linear-gradient(135deg, #ff9933, #ffffff, #138808);
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 3px 8px rgba(0,0,0,0.2);
        }

        header h1 {
            font-size: 3em;
            margin-bottom: 10px;
            text-shadow: 3px 3px 5px rgba(0,0,0,0.4);
            font-weight: bold;
        }

        header h1 span:nth-child(1) { color: #ff9933; } /* A */
        header h1 span:nth-child(2) { color: #ffffff; } /* L */
        header h1 span:nth-child(3) { color: #138808; } /* L */
        header h1 span:nth-child(4) { color: #ff4500; } /* E */
        header h1 span:nth-child(5) { color: #00ced1; } /* X */
        header h1 span:nth-child(6) { color: #ff69b4; } /* A */
        header h1 span:nth-child(7) { color: #20b2aa; } /* M */
        header h1 span:nth-child(8) { color: #ff8c00; } /* I */
        header h1 span:nth-child(9) { color: #6a5acd; } /* N */
        header h1 span:nth-child(10) { color: #ff1493; } /* D */
        header h1 span:nth-child(11) { color: #32cd32; } /* I */
        header h1 span:nth-child(12) { color: #ff4500; } /* A */

        .ticker {
            background: linear-gradient(90deg, #ffeb3b, #ff9800);
            color: #333;
            padding: 12px;
            font-size: 1.3em;
            font-weight: bold;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .ticker marquee {
            width: 100%;
        }

        header nav {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 10px;
        }

        header nav a {
            color: white;
            text-decoration: none;
            font-size: 1.2em;
            padding: 12px 25px;
            border-radius: 30px;
            background: linear-gradient(45deg, #ff4500, #32cd32);
            transition: transform 0.3s;
        }

        header nav a:hover {
            transform: scale(1.1);
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            padding: 30px;
            max-width: 1200px;
            margin: 20px auto;
        }

        .category-card {
            background: linear-gradient(135deg, #4caf50, #2196f3);
            color: white;
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            cursor: pointer;
            box-shadow: 0 6px 15px rgba(0,0,0,0.25);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .category-card:nth-child(2) { background: linear-gradient(135deg, #ff9800, #f44336); }
        .category-card:nth-child(3) { background: linear-gradient(135deg, #9c27b0, #3f51b5); }
        .category-card:nth-child(4) { background: linear-gradient(135deg, #00bcd4, #009688); }
        .category-card:nth-child(5) { background: linear-gradient(135deg, #ffeb3b, #ff5722); }

        .category-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }

        .category-card h2 {
            font-size: 1.8em;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
        }

        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 0 15px;
        }

        .category-section {
            display: none;
            margin-bottom: 40px;
            background: white;
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.15);
            transition: transform 0.3s;
        }

        .category-section.active {
            display: block;
        }

        .category-section h2 {
            color: #3f51b5;
            font-size: 2em;
            margin-bottom: 20px;
            border-bottom: 4px solid #ff6f61;
            padding-bottom: 8px;
        }

        .question {
            background: #f9f9f9;
            border: 1px solid #ddd;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 25px;
            transition: box-shadow 0.3s;
        }

        .question:hover {
            box-shadow: 0 6px 12px rgba(0,0,0,0.15);
        }

        .question h3 {
            font-size: 1.6em;
            margin-bottom: 12px;
            color: #333;
        }

        .options {
            list-style-type: none;
            margin-bottom: 12px;
        }

        .options li {
            margin-bottom: 10px;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 10px;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s;
        }

        .options li:hover {
            background: #e3f2fd;
            transform: translateX(6px);
        }

        .answer {
            display: none;
            background: #d1e7dd;
            padding: 12px;
            border-radius: 10px;
            margin-top: 12px;
            color: #0f5132;
            font-weight: 500;
        }

        .show-answer {
            background: #ff6f61;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 30px;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s;
        }

        .show-answer:hover {
            background: #e55a50;
            transform: scale(1.05);
        }

        .ad-placeholder {
            background: #f0f0f0;
            padding: 20px;
            text-align: center;
            border-radius: 10px;
            margin-top: 20px;
        }

        footer {
            background: linear-gradient(90deg, #3f51b5, #ff6f61);
            color: white;
            text-align: center;
            padding: 25px;
            margin-top: 40px;
            border-radius: 0 0 20px 20px;
        }

        footer p {
            font-size: 1.2em;
            font-weight: bold;
        }

        .email-icon {
            font-size: 1.5em;
            cursor: pointer;
            transition: color 0.3s;
        }

        .email-icon:hover {
            color: #ffeb3b;
        }

        .hidden-email {
            display: none;
            margin-top: 10px;
        }

        @media (max-width: 768px) {
            header h1 { font-size: 2.2em; }
            header nav { flex-direction: column; gap: 12px; }
            .ticker { font-size: 1.1em; }
            .question h3 { font-size: 1.4em; }
            .category-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <header>
        <h1>
            <span>A</span><span>L</span><span>L</span>
            <span>E</span><span>X</span><span>A</span><span>M</span>
            <span>I</span><span>N</span><span>D</span><span>I</span><span>A</span>
        </h1>
        <div class='ticker'>
            <marquee behavior='scroll' direction='left'>Current Affairs (03:22 PM +04, 25 Aug 2025): प्र. 1: भारत का वर्तमान राष्ट्रपति कौन है? (A) रामनाथ कोविंद (B) द्रौपदी मुर्मू (C) प्रणब मुखर्जी (D) एपीजे अब्दुल कलाम | उत्तर: B</marquee>
        </div>
        <nav>
            <a href='#' onclick='showHome(); return false;'>Home</a>
        </nav>
    </header>

    <div id='home' class='category-grid'>
        <div class='category-card' onclick='showCategory("gk")'>
            <h2>GK GS</h2>
        </div>
        <div class='category-card' onclick='showCategory("daroga")'>
            <h2>Bihar Police Daroga</h2>
        </div>
        <div class='category-card' onclick='showCategory("constable")'>
            <h2>Bihar Police Constable</h2>
        </div>
        <div class='category-card' onclick='showCategory("math")'>
            <h2>Math</h2>
        </div>
        <div class='category-card' onclick='showCategory("science")'>
            <h2>Science</h2>
        </div>
    </div>

    <div class='container'>
        <section id='gk' class='category-section'>
            <h2>GK GS</h2>
            <div class='question'>
                <h3>प्रश्न 1: भारत का राष्ट्रीय ध्वज तिरंगा कब अपनाया गया?</h3>
                <ul class='options'>
                    <li>A) 15 अगस्त 1947</li>
                    <li>B) 26 जनवरी 1950</li>
                    <li>C) 22 जुलाई 1947</li>
                    <li>D) 26 नवंबर 1949</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: C) 22 जुलाई 1947</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 2: बिहार का सबसे बड़ा जिला (क्षेत्रफल के हिसाब से) कौन सा है?</h3>
                <ul class='options'>
                    <li>A) गया</li>
                    <li>B) पश्चिम चंपारण</li>
                    <li>C) पटना</li>
                    <li>D) मुजफ्फरपुर</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) पश्चिम चंपारण</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 3: भारत की राजधानी कौन सी है?</h3>
                <ul class='options'>
                    <li>A) मुंबई</li>
                    <li>B) कोलकाता</li>
                    <li>C) नई दिल्ली</li>
                    <li>D) चेन्नई</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: C) नई दिल्ली</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 4: विश्व का सबसे ऊंचा पर्वत कौन सा है?</h3>
                <ul class='options'>
                    <li>A) कंचनजंगा</li>
                    <li>B) एवरेस्ट</li>
                    <li>C) क2</li>
                    <li>D) मकालू</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) एवरेस्ट</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 5: भारत का राष्ट्रीय पशु कौन सा है?</h3>
                <ul class='options'>
                    <li>A) शेर</li>
                    <li>B) हाथी</li>
                    <li>C) बाघ</li>
                    <li>D) गाय</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: C) बाघ</div>
            </div>
            <!-- Add more questions up to 50 following the same pattern -->
            <div class='ad-placeholder'>
                <p>यहां आपका विज्ञापन (Ad) दिखेगा। [Google AdSense या अन्य कोड डालें]</p>
            </div>
        </section>

        <section id='daroga' class='category-section'>
            <h2>Bihar Police Daroga</h2>
            <div class='question'>
                <h3>प्रश्न 1: बिहार पुलिस दरोगा भर्ती में प्रारंभिक परीक्षा में कितने प्रश्न पूछे जाते हैं?</h3>
                <ul class='options'>
                    <li>A) 100</li>
                    <li>B) 150</li>
                    <li>C) 200</li>
                    <li>D) 75</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: A) 100</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 2: बिहार पुलिस दरोगा भर्ती में शारीरिक दक्षता परीक्षा में पुरुषों के लिए दौड़ कितनी दूरी की होती है?</h3>
                <ul class='options'>
                    <li>A) 1.6 किमी</li>
                    <li>B) 1 किमी</li>
                    <li>C) 2 किमी</li>
                    <li>D) 800 मीटर</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: A) 1.6 किमी</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 3: बिहार पुलिस दरोगा भर्ती की आयु सीमा क्या है?</h3>
                <ul class='options'>
                    <li>A) 18-25 वर्ष</li>
                    <li>B) 20-27 वर्ष</li>
                    <li>C) 21-30 वर्ष</li>
                    <li>D) 25-35 वर्ष</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 20-27 वर्ष</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 4: दरोगा भर्ती में लिखित परीक्षा का समय कितना है?</h3>
                <ul class='options'>
                    <li>A) 1 घंटा</li>
                    <li>B) 2 घंटे</li>
                    <li>C) 3 घंटे</li>
                    <li>D) 4 घंटे</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 2 घंटे</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 5: दरोगा भर्ती में न्यूनतम शैक्षिक योग्यता क्या है?</h3>
                <ul class='options'>
                    <li>A) 10वीं पास</li>
                    <li>B) 12वीं पास</li>
                    <li>C) स्नातक</li>
                    <li>D) डिप्लोमा</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: C) स्नातक</div>
            </div>
            <!-- Add more questions up to 50 following the same pattern -->
            <div class='ad-placeholder'>
                <p>यहां आपका विज्ञापन (Ad) दिखेगा। [Google AdSense या अन्य कोड डालें]</p>
            </div>
        </section>

        <section id='constable' class='category-section'>
            <h2>Bihar Police Constable</h2>
            <div class='question'>
                <h3>प्रश्न 1: बिहार पुलिस कांस्टेबल भर्ती परीक्षा में कुल कितने अंक होते हैं?</h3>
                <ul class='options'>
                    <li>A) 100</li>
                    <li>B) 150</li>
                    <li>C) 200</li>
                    <li>D) 75</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: A) 100</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 2: बिहार पुलिस कांस्टेबल भर्ती में लिखित परीक्षा में नकारात्मक अंकन कितना होता है?</h3>
                <ul class='options'>
                    <li>A) 0.2 अंक</li>
                    <li>B) 0.25 अंक</li>
                    <li>C) 0.5 अंक</li>
                    <li>D) कोई नकारात्मक अंकन नहीं</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 0.25 अंक</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 3: कांस्टेबल भर्ती के लिए आयु सीमा क्या है?</h3>
                <ul class='options'>
                    <li>A) 18-25 वर्ष</li>
                    <li>B) 20-27 वर्ष</li>
                    <li>C) 21-30 वर्ष</li>
                    <li>D) 25-35 वर्ष</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: A) 18-25 वर्ष</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 4: कांस्टेबल भर्ती में शारीरिक दक्षता परीक्षा में पुरुषों के लिए दौड़ की दूरी क्या है?</h3>
                <ul class='options'>
                    <li>A) 1.6 किमी</li>
                    <li>B) 1 किमी</li>
                    <li>C) 2 किमी</li>
                    <li>D) 800 मीटर</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: A) 1.6 किमी</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 5: कांस्टेबल भर्ती के लिए न्यूनतम शैक्षिक योग्यता क्या है?</h3>
                <ul class='options'>
                    <li>A) 10वीं पास</li>
                    <li>B) 12वीं पास</li>
                    <li>C) स्नातक</li>
                    <li>D) डिप्लोमा</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 12वीं पास</div>
            </div>
            <!-- Add more questions up to 50 following the same pattern -->
            <div class='ad-placeholder'>
                <p>यहां आपका विज्ञापन (Ad) दिखेगा। [Google AdSense या अन्य कोड डालें]</p>
            </div>
        </section>

        <section id='math' class='category-section'>
            <h2>गणित</h2>
            <div class='question'>
                <h3>प्रश्न 1: 2 + 2 का परिणाम क्या होगा?</h3>
                <ul class='options'>
                    <li>A) 3</li>
                    <li>B) 4</li>
                    <li>C) 5</li>
                    <li>D) 6</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 4</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 2: 5 × 6 का परिणाम क्या होगा?</h3>
                <ul class='options'>
                    <li>A) 25</li>
                    <li>B) 30</li>
                    <li>C) 35</li>
                    <li>D) 40</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 30</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 3: 100 ÷ 4 का परिणाम क्या होगा?</h3>
                <ul class='options'>
                    <li>A) 20</li>
                    <li>B) 25</li>
                    <li>C) 30</li>
                    <li>D) 15</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 25</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 4: 7 का वर्ग क्या होगा?</h3>
                <ul class='options'>
                    <li>A) 42</li>
                    <li>B) 49</li>
                    <li>C) 56</li>
                    <li>D) 63</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 49</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 5: 10% का 200 क्या होगा?</h3>
                <ul class='options'>
                    <li>A) 10</li>
                    <li>B) 20</li>
                    <li>C) 30</li>
                    <li>D) 40</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: B) 20</div>
            </div>
            <!-- Add more questions up to 50 following the same pattern -->
            <div class='ad-placeholder'>
                <p>यहां आपका विज्ञापन (Ad) दिखेगा। [Google AdSense या अन्य कोड डालें]</p>
            </div>
        </section>

        <section id='science' class='category-section'>
            <h2>विज्ञान</h2>
            <div class='question'>
                <h3>प्रश्न 1: पानी का रासायनिक सूत्र क्या है?</h3>
                <ul class='options'>
                    <li>A) H2O</li>
                    <li>B) CO2</li>
                    <li>C) O2</li>
                    <li>D) NaCl</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: A) H2O</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 2: सूर्य का सबसे निकटतम ग्रह कौन सा है?</h3>
                <ul class='options'>
                    <li>A) पृथ्वी</li>
                    <li>B) मंगल</li>
                    <li>C) बुध</li>
                    <li>D) शुक्र</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: C) बुध</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 3: मानव शरीर में सबसे बड़ा अंग कौन सा है?</h3>
                <ul class='options'>
                    <li>A) हृदय</li>
                    <li>B) यकृत</li>
                    <li>C) त्वचा</li>
                    <li>D) फेफड़े</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: C) त्वचा</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 4: ऑक्सीजन का रासायनिक चिह्न क्या है?</h3>
                <ul class='options'>
                    <li>A) O</li>
                    <li>B) Ox</li>
                    <li>C) Oy</li>
                    <li>D) Og</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: A) O</div>
            </div>
            <div class='question'>
                <h3>प्रश्न 5: प्रकाश की गति कितनी है?</h3>
                <ul class='options'>
                    <li>A) 300,000 किमी/सेकंड</li>
                    <li>B) 150,000 किमी/सेकंड</li>
                    <li>C) 500,000 किमी/सेकंड</li>
                    <li>D) 100,000 किमी/सेकंड</li>
                </ul>
                <button class='show-answer' onclick='toggleAnswer(this)'>उत्तर दिखाएं</button>
                <div class='answer'>उत्तर: A) 300,000 किमी/सेकंड</div>
            </div>
            <!-- Add more questions up to 50 following the same pattern -->
            <div class='ad-placeholder'>
                <p>यहां आपका विज्ञापन (Ad) दिखेगा। [Google AdSense या अन्य कोड डालें]</p>
            </div>
        </section>
    </div>

    <footer>
        <p>Made by Azad</p>
        <i class="fas fa-envelope email-icon" onclick="toggleEmail()"></i>
        <p id="contact-email" class="hidden-email">Contact: <a href="mailto:ansariazad681@gmail.com">ansariazad681@gmail.com</a></p>
    </footer>

    <script>
        function toggleAnswer(button) {
            var answer = button.nextElementSibling;
            if (answer.style.display === "block") {
                answer.style.display = "none";
                button.textContent = "उत्तर दिखाएं";
            } else {
                answer.style.display = "block";
                button.textContent = "उत्तर छिपाएं";
            }
        }

        function showHome() {
            document.getElementById('home').style.display = 'grid';
            document.querySelectorAll('.category-section').forEach(function(section) {
                section.classList.remove('active');
            });
        }

        function showCategory(categoryId) {
            document.getElementById('home').style.display = 'none';
            document.querySelectorAll('.category-section').forEach(function(section) {
                section.classList.remove('active');
            });
            document.getElementById(categoryId).classList.add('active');
        }

        function toggleEmail() {
            var email = document.getElementById('contact-email');
            if (email.style.display === "block") {
                email.style.display = "none";
            } else {
                email.style.display = "block";
            }
        }

        window.onload = showHome;
    </script>
</body>
</html>
