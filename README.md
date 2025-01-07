
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>صدقة جارية للمرحوم الحبيب محمد احمد حامد زياده</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background-image: url('myimage.jpg'); /* تأكد من وجود الصورة */
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: #fff;
            text-align: center;
        }

        .content {
            padding: 20px;
        }

        h1 {
            margin-top: 50px;
            font-size: 36px;
        }

        .tasbeeh-counter {
            background: rgba(0, 0, 0, 0.7);
            padding: 20px;
            border-radius: 10px;
            margin: 20px auto;
            width: 80%;
            max-width: 600px;
        }

        .tasbeeh-counter button {
            margin: 5px;
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .footer {
            margin-top: 50px;
            font-size: 14px;
            color: #ccc;
        }

        .reminder, .duas, .special-prayer {
            margin-top: 30px;
            font-size: 20px;
            color: #ffeb3b;
            font-weight: bold;
        }

        .duas {
            font-size: 18px;
            color: #fff;
            line-height: 1.8;
            font-weight: normal;
        }

        .special-prayer {
            font-size: 18px;
            color: #ff4081;
            font-weight: bold;
            margin-top: 30px;
        }
    </style>
</head>
<body>
    <!-- تشغيل الصوت -->
    <audio id="background-audio" autoplay loop muted>
        <source src="dua.mp3" type="audio/mp3">
        متصفحك لا يدعم الصوت.
    </audio>

    <script>
        // إزالة الكتم وتشغيل الصوت بعد أول تفاعل مع الصفحة
        window.addEventListener('click', function () {
            const audio = document.getElementById('background-audio');
            audio.muted = false;
            audio.play();
        });
    </script>

    <!-- محتوى الموقع -->
    <div class="content">
        <h1>صدقة جارية على روح المرحوم الحبيب محمد احمد حامد زياده</h1>

        <div class="tasbeeh-counter">
            <h2>عداد التسبيح</h2>
            
            <!-- تسبيحة سبحان الله -->
            <p>سبحان الله</p>
            <button onclick="incrementCounter('subhan')">زود في مثقال حسناتي</button>
            <p>العدد: <span id="counter-subhan">0</span></p>

            <!-- تسبيحة الحمد لله -->
            <p>الحمد لله</p>
            <button onclick="incrementCounter('alhamd')">زود في مثقال حسناتي</button>
            <p>العدد: <span id="counter-alhamd">0</span></p>

            <!-- تسبيحة لا إله إلا الله -->
            <p>لا إله إلا الله</p>
            <button onclick="incrementCounter('la-ilaha')">زود في مثقال حسناتي</button>
            <p>العدد: <span id="counter-la-ilaha">0</span></p>

            <!-- تسبيحة الله أكبر -->
            <p>الله أكبر</p>
            <button onclick="incrementCounter('allah-akbar')">زود في مثقال حسناتي</button>
            <p>العدد: <span id="counter-allah-akbar">0</span></p>

            <!-- زر تصفير جميع العدادات -->
            <button onclick="resetCounters()">تصفير العداد</button>
        </div>

        <!-- خانة النص -->
        <div class="reminder">
            وإن غبت يا صاحبي متنسانيش من دعائك
        </div>

        <!-- خانة الأدعية للمتوفى -->
        <div class="duas">
            <h3>أدعية للمتوفي</h3>
            <p>
                اللهم اغفر له وارحمه، وعافه واعفُ عنه، وأكرم نزله، ووسع مدخله، واغسله بالماء والثلج والبرد، ونقِه من الذنوب والخطايا كما ينقى الثوب الأبيض من الدنس.
            </p>
            <p>
                اللهم اجعل قبره روضة من رياض الجنة، ولا تجعله حفرة من حفر النار.
            </p>
            <p>
                اللهم اجعل دعاءنا له صدقة جارية، واغفر له ما تقدم من ذنبه وما تأخر.
            </p>
            <p>
                اللهم ارزقنا جميعًا حسن الخاتمة، واجعلنا من أهل الجنة.
            </p>
        </div>

        <!-- خانة الثواب -->
        <div class="special-prayer">
            اللهم اجعل ثواب هذه الأذكار في مثقال حسنات المغفور له بإذن الله.  
            هتفضل في القلب دايماً يا أبو حامد 🖤
        </div>

        <div class="footer">
            <p> صمم الموقع بواسطة محبك في الله: باسم حماده</p>
        </div>
    </div>

    <script>
        // تعريف العدادات
        let counters = {
            'subhan': 0,
            'alhamd': 0,
            'la-ilaha': 0,
            'allah-akbar': 0
        };

        // دالة لزيادة العداد
        function incrementCounter(dhikr) {
            if (counters[dhikr] < 33) { // لا يزيد عن 33
                counters[dhikr]++;
                document.getElementById('counter-' + dhikr).innerText = counters[dhikr];
            }
        }

        // دالة لتصفير العدادات
        function resetCounters() {
            counters = {
                'subhan': 0,
                'alhamd': 0,
                'la-ilaha': 0,
                'allah-akbar': 0
            };
            document.getElementById('counter-subhan').innerText = counters['subhan'];
            document.getElementById('counter-alhamd').innerText = counters['alhamd'];
            document.getElementById('counter-la-ilaha').innerText = counters['la-ilaha'];
            document.getElementById('counter-allah-akbar').innerText = counters['allah-akbar'];
        }
    </script>
</body>
</html>
