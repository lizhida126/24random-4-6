<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>アンケートにご協力ください</title>
    <style>
        body {
            font-family: "Hiragino Kaku Gothic ProN", "Hiragino Sans", Meiryo, sans-serif;
            text-align: center;
            padding-top: 80px;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
        }
        .container {
            background: #fff;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            max-width: 480px;
            margin: auto;
            width: 90%;
        }
        h1 {
            color: #007bff;
            font-size: 22px;
            margin-bottom: 20px;
        }
        p {
            font-size: 15px;
            color: #555;
            line-height: 1.8;
            margin-bottom: 10px;
        }
        .loading {
            margin-top: 30px;
            font-size: 13px;
            color: #888;
        }
        /* 简单的加载动画圆圈 */
        .spinner {
            margin: 20px auto;
            width: 40px;
            height: 40px;
            border: 4px solid #f3f3f3;
            border-top: 4px solid #007bff;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>

<div class="container">
    <h1>アンケート準備中</h1>
    <p>ただいま、アンケートフォームへ移動しています。<br>画面を閉じずにお待ちください。</p>
    
    <div class="spinner"></div>
    <div class="loading">Redirecting to survey...</div>

    <script>
        // =======================================================
        // ▼▼▼ 4组问卷链接配置区域 (已更新) ▼▼▼
        // =======================================================
        
        const forms = [
            'https://docs.google.com/forms/d/e/1FAIpQLSfaTUDp6Og5PCohyRvA7bfHiYGxPPYzg6gX4J1lWs4G3W4qAQ/viewform?usp=header',
            'https://docs.google.com/forms/d/e/1FAIpQLScvEMi2FMaCm06ya5GObWvBFiho0SCdmqIPNHEhaXFCIhrXzQ/viewform?usp=header',
            'https://docs.google.com/forms/d/e/1FAIpQLSdtI-L0n7ZSW-hWCv6wRh0_A_l4uPX0HHZW_0MlcCv7bUrpfg/viewform?usp=header',
            'https://docs.google.com/forms/d/e/1FAIpQLSfkXbyTKUd4I-gj2cRKUgBa7qr73Vg5z1SIGmWbbQ5Iq4sBhg/viewform?usp=header'
        ];

        // =======================================================
        // ▲▲▲ 配置结束 ▲▲▲
        // =======================================================

        // 1. 随机逻辑：生成 0 到 3 之间的随机整数
        const randomIndex = Math.floor(Math.random() * forms.length); 

        // 2. 获取目标链接
        const targetUrl = forms[randomIndex];

        // 3. (可选) 调试信息
        console.log(`Random Group: ${randomIndex + 1}`);
        console.log(`Target URL: ${targetUrl}`);
        
        // 4. 执行跳转 (延迟 800ms 让用户看到提示，体验更平滑)
        setTimeout(function() {
             window.location.replace(targetUrl);
        }, 800);

    </script>
</div>

</body>
</html>
