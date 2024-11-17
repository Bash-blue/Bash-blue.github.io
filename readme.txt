<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./index.css">
    <style>
        .content {
            display: none;
        }
        #home-content {
            display: block; /* 默认显示Home内容 */
        }
    </style>
</head>
<body>

    <div class="navbar">
        <a href="#home" class="nav-link">Home</a>
        <a href="#about" class="nav-link">About</a>
        <a href="#services" class="nav-link">Services</a>
        <a href="#portfolio" class="nav-link">Portfolio</a>
        <a href="#contact" class="nav-link">Contact</a>
    </div>
    
    <div class="content" id="home-content">
        <h1>My Personal Portfolio</h1>
        <h2>Featured Projects</h2>
        <!-- Home content -->
    </div>
    <div class="content" id="about-content">
        <div class="content">
            <h1>My Personal Portfolio</h1>
            <h2>Featured Projects</h2>
            <div class="project">
                <img src="./image/手风琴.png" alt="Project Image">
                <h3 class="project-title">Accordion (手风琴)</h3>
                <p class="project-description">A responsive accordion component for your web projects.</p>
                <a href="./demo/手风琴.html">View Project</a>
            </div>
            <!-- Add more project divs as needed -->
            <div class="project">
                <img src="https://via.placeholder.com/150" alt="Project Image">
                <h3 class="project-title">Placeholder for Future Project</h3>
                <p class="project-description">Description of your future project goes here.</p>
                <a href="#">View Project</a>
            </div>
        </div>
    </div>
    <div class="content" id="services-content">
        <!-- Services content -->
    </div>
    <div class="content" id="portfolio-content">
        <!-- Portfolio content -->
    </div>
    <div class="content" id="contact-content">
        <!-- Contact content -->
    </div>
    
    <script>
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault(); // 阻止默认的链接跳转行为
                const contentId = this.getAttribute('href').slice(1); // 获取href属性中的ID
                document.querySelectorAll('.content').forEach(content => {
                    content.style.display = 'none'; // 隐藏所有内容
                });
                document.getElementById(contentId + '-content').style.display = 'block'; // 显示对应的内容
            });
        });
    </script>
</body>
</html>