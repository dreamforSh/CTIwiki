# 开发测试页



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS 示例</title>
    <style>
        /* 设置 body 的字体、背景颜色和行高 */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }

        /* 设置标题的样式 */
        h1 {
            color: #333;
            text-align: center;
            margin-top: 20px;
        }

        /* 设置段落的样式 */
        p {
            font-size: 16px;
            color: #666;
            margin: 10px 20px;
            text-indent: 2em; /* 首行缩进 */
        }

        /* 设置容器的样式 */
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        /* 设置链接的样式 */
        a {
            color: #007bff;
            text-decoration: none;
        }

        /* 鼠标悬停在链接上的样式 */
        a:hover {
            text-decoration: underline;
        }

        /* 设置按钮的样式 */
        .btn {
            display: inline-block;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }

        /* 设置按钮的悬停效果 */
        .btn:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>欢迎来到我的网页</h1>
        <p>这是一个使用 CSS 样式的简单示例。</p>
        <a href="https://www.example.com">访问示例链接</a>
        <button class="btn">点击我</button>
    </div>
</body>
</html>
```
