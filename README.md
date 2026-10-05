<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <title>نظام المبيعات</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, Tahoma, sans-serif;
            background: #f5f7fa;
            color: #222;
        }

        .container {
            display: flex;
            min-height: 100vh;
        }

        /* القائمة الجانبية */
        .sidebar {
            width: 230px;
            background: white;
            border-left: 1px solid #ddd;
            padding: 20px;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #1687a7;
            margin-bottom: 30px;
        }

        .menu button {
            width: 100%;
            border: none;
            background: transparent;
            padding: 14px;
            margin-bottom: 8px;
            text-align: right;
            border-radius: 10px;
            cursor: pointer;
            font-size: 16px;
        }

        .menu button:hover,
        .menu button.active {
            background: #e8f6f9;
            color: #1687a7;
        }

        /* المحتوى */
        .content {
            flex: 1;
            padding: 30px;
        }

        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .header h1 {
            font-size: 28px;
        }

        .button {
            background: #1687a7;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 10px;
            cursor: pointer;
        }

        /* البطاقات */
        .cards {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
        }

        .card {
            background: white;
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #eee;
        }

        .card-title {
            color: #777;
            margin-bottom: 10px;
        }

        .card-value {
            font-size: 25px;
            font-weight: bold;
        }

        /* الأقسام */
        .section {
            background: white;
            margin-top: 20px;
            padding: 20px;
            border-radius: 15px;
        }

        .section h2 {
            margin-bottom: 15px;
        }

        /* للموبايل */
        @media (max-width: 800px) {

            .sidebar {
                width: 75px;
                padding: 10px;
            }

            .logo {
                font-size: 0;
            }

            .logo::after {
                content: "🛒";
                font-size: 25px;
            }

            .menu span {
                display: none;
            }

            .menu button {
                text-align: center;
            }

            .content {
                padding: 15px;
            }

            .cards {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 500px) {

            .cards {
                grid-template-columns: 1fr;
            }

            .header {
                flex-direction: column;
                align-items: flex-start;
                gap: 15px;
            }
        }
    </style>
</head>

<body>

<div class="container">

    <!-- القائمة -->
    <aside class="sidebar">

        <div class="logo">
            🛒 مبيعات
        </div>

        <div class="menu">

            <button class="active">
                🏠 <span>الرئيسية</span>
            </button>

            <button>
                🛒 <span>بيع</span>
            </button>

            <button>
                📦 <span>المنتجات</span>
            </button>

            <button>
                💰 <span>الحسابات</span>
            </button>

            <button>
                ⚙️ <span>الإعدادات</span>
            </button>

        </div>

    </aside>


    <!-- المحتوى -->
    <main class="content">

        <div class="header">

            <div>
                <h1>الرئيسية</h1>
                <p>ملخص المبيعات اليوم</p>
            </div>

            <button class="button">
                + بيع جديد
            </button>

        </div>


        <!-- البطاقات -->
        <div class="cards">

            <div class="card">
                <div class="card-title">
                    مبيعات اليوم
                </div>

                <div class="card-value">
                    0 ج.م
                </div>
            </div>


            <div class="card">
                <div class="card-title">
                    الأرباح
                </div>

                <div class="card-value">
                    0 ج.م
                </div>
            </div>


            <div class="card">
                <div class="card-title">
                    المنتجات
                </div>

                <div class="card-value">
                    0
                </div>
            </div>


            <div class="card">
                <div class="card-title">
                    الديون
                </div>

                <div class="card-value">
                    0 ج.م
                </div>
            </div>

        </div>


        <!-- آخر المبيعات -->
        <div class="section">

            <h2>
                آخر المبيعات
            </h2>

            <p>
                لا توجد مبيعات حتى الآن.
            </p>

        </div>

    </main>

</div>

</body>
</html>
