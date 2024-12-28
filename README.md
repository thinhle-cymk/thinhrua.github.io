<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pháo hoa</title>
    <style>
        body,
        html {
            height: 100%;
            width: 100%;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
            overflow: hidden;
            flex-direction: column;
            text-align: center;
            position: relative;
        }
        #c {
            background-color: #ffffff;
        }
        canvas {
            position: absolute;
            top: 0;
            left: 0;
            z-index: -1;
        }

        #btn {
            height: 55px;
            width: 75px;
            cursor: pointer;
            background-color: #ce4f6a00;
            color: white;
            border: none;
            border-radius: 10px;
            transition: all 0.3s ease-in-out;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: opacity 0.3s ease;
        }

        #btnYes,
        #btnNo {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            background-color: #ce4f6a;
            color: white;
            border: none;
            border-radius: 10px;
            transition: all 0.3s ease-in-out;
            margin: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        h1,
        p {
            transition: opacity 0.3s ease;
            font-family: 'Times New Roman', 'Arial', sans-serif;
        }

        .hide {
            display: none;
        }

        .show {
            opacity: 1;
        }

        #btn img {
            width: 60px;
            height: 40px;
        }

        @keyframes shake {
            0% {
                transform: translateX(0);
            }

            25% {
                transform: translateX(-5px);
            }

            50% {
                transform: translateX(5px);
            }

            75% {
                transform: translateX(-5px);
            }

            100% {
                transform: translateX(5px);
            }
        }

        .shake {
            animation: shake 0.5s ease-in-out;
        }

        #btn:hover,
        #btnYes:hover,
        #btnNo:hover {
            background-color: #d37da8;
            transform: translateY(-4px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        }

        #btn:active,
        #btnYes:active,
        #btnNo:active {
            transform: translateY(2px);
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.2);
        }

        .message {
            display: none;
            font-size: 20px;
            margin: 10px;
            padding: 30px;
            border: 2px solid #f19fb3;
            border-radius: 8px;
            background-color: #ffffff;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 90%;
            overflow: hidden;
            word-wrap: break-word;
            transform: perspective(500px) rotateY(10deg);
            transition: all 0.3s ease-in-out;
        }

        .message.show {
            transform: perspective(500px) rotateY(0deg);
        }

        .div-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            max-width: 100%;
            overflow: hidden;
            margin: 10px 0;
        }

        .message-text {
            font-size: 18px;
            display: block;
            padding: 30px;
            border: 2px solid #f19fb3;
            border-radius: 10px;
            background-color: #ffffff;
            text-align: center;
            margin-bottom: 30px;
            transform: perspective(500px) rotateY(10deg);
            transition: all 0.3s ease-in-out;
        }

        .message-text.show {
            transform: perspective(500px) rotateY(0deg);
        }
    </style>
</head>

<body>
    <canvas id="c" width="948" height="586"></canvas>
    <div>
        <h1 id="messageTitle">Bạn có tin nhắn mới</h1>
        <p id="messageText">Xem ngay</p>
        <button id="btn">
            <img src="./letters.png" alt="Description">
        </button>
        <div class="message">Em à</div>
        <div class="message">Còn vài ngày nữa là hết năm rồi nhỉ!</div>
        <div class="message">Tối ngày 31 có một buổi pháo hoa đẹp lắm</div>
        <div class="message">anh nghĩ chẳng có gì tuyệt vời hơn việc bên cạnh em,</div>
        <div class="message">nhìn những ánh sáng rực rỡ trên bầu trời.</div>
        <div class="message">🌟 Em có muốn cùng anh đi không?</div>
        <div class="message">Anh hứa sẽ không để em phải chờ lâu đâu,</div>
        <div class="message">anh muốn được nhìn thấy nụ cười của em khi pháo hoa nở rộ. 😘</div>

        <div id="msgYes" class="message-text" style="display: none;">Chắc chắn buổi tối đó sẽ còn đặc biệt hơn nếu có em bên cạnh. 💕</div>

        <div class="div-buttons">
            <button id="btnYes" style="display: none;">Ok anh</button>
            <button id="btnNo" style="display: none;">Suy nghĩ</button>
        </div>
    </div>
    <script src="./script.js"></script>

</body>

</html>
