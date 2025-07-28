<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello Kitty 自定义导航站</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600&display=swap">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary-pink: #ff77a8;
            --secondary-pink: #ffafc7;
            --background-color: #fff6f9;
            --light-pink: #ffeaf0;
            --dark-pink: #e84393;
            --white: #ffffff;
            --gray: #888;
            --shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        
        body {
            font-family: 'Poppins', 'Microsoft YaHei', sans-serif;
            background-color: var(--background-color);
            background-image: url("data:image/svg+xml,%3Csvg width='80' height='80' viewBox='0 0 80 80' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffafc7' fill-opacity='0.2'%3E%3Cpath d='M50 50c0-5.523 4.477-10 10-10s10 4.477 10 10-4.477 10-10 10c0 5.523-4.477 10-10 10s-10-4.477-10-10 4.477-10 10-10zM10 10c0-5.523 4.477-10 10-10s10 4.477 10 10-4.477 10-10 10c0 5.523-4.477 10-10 10S0 25.523 0 20s4.477-10 10-10zm10 8c4.418 0 8-3.582 8-8s-3.582-8-8-8-8 3.582-8 8 3.582 8 8 8zm40 40c4.418 0 8-3.582 8-8s-3.582-8-8-8-8 3.582-8 8 3.582 8 8 8z' /%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
            color: #333;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 20px 0 30px;
            position: relative;
        }
        
        .hello-kitty {
            position: absolute;
            left: 20px;
            top: 10px;
            font-size: 40px;
        }
        
        h1 {
            font-size: 2.8rem;
            color: var(--dark-pink);
            margin-bottom: 10px;
            position: relative;
            display: inline-block;
        }
        
        h1::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 120px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-pink), var(--light-pink));
            border-radius: 2px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: var(--dark-pink);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .actions {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 25px 0;
        }
        
        button {
            background: var(--primary-pink);
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 1rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
            box-shadow: var(--shadow);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        button:hover {
            background: var(--dark-pink);
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(232, 67, 147, 0.3);
        }
        
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }
        
        .site-card {
            background: var(--white);
            border-radius: 15px;
            padding: 25px 15px;
            box-shadow: var(--shadow);
            transition: all 0.3s ease;
            text-align: center;
            position: relative;
            overflow: hidden;
            border: 2px solid var(--light-pink);
        }
        
        .site-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 20px rgba(232, 67, 147, 0.2);
            border-color: var(--primary-pink);
        }
        
        .site-card::before {
            content: '❤';
            position: absolute;
            top: -10px;
            right: 10px;
            font-size: 20px;
            color: var(--primary-pink);
        }
        
        .site-icon {
            width: 70px;
            height: 70px;
            background: var(--light-pink);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 15px;
            font-size: 30px;
            color: var(--dark-pink);
            overflow: hidden;
            border: 2px solid var(--sec
