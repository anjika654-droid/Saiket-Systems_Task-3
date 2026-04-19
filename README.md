# Saiket-Systems_Task-3
Design a webpage with four sections: a header, a sidebar, a main content area, and a footer. Use CSS to make the layout responsive, ensuring it looks good on all screen sizes. Apply media queries to switch between a grid layout for desktops and a stacked layout for mobile devices

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Responsive Layout</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

/* Main Container */
.container{
    display:grid;
    grid-template-columns:250px 1fr;
    grid-template-rows:auto 1fr auto;
    grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
    height:100vh;
}

/* Sections */
header{
    grid-area:header;
    background:#007bff;
    color:white;
    padding:20px;
    text-align:center;
}

aside{
    grid-area:sidebar;
    background:#f4f4f4;
    padding:20px;
}

main{
    grid-area:main;
    padding:20px;
    background:#ffffff;
}

footer{
    grid-area:footer;
    background:#333;
    color:white;
    text-align:center;
    padding:15px;
}

/* Responsive Mobile Layout */
@media(max-width:768px){

.container{
    grid-template-columns:1fr;
    grid-template-areas:
        "header"
        "main"
        "sidebar"
        "footer";
}

aside{
    background:#e9ecef;
}

}
</style>
</head>

<body>

<div class="container">

<header>
    <h1>My Responsive Website</h1>
</header>

<aside>
    <h3>Sidebar</h3>
    <p>Navigation links or extra content here.</p>
</aside>

<main>
    <h2>Main Content</h2>
    <p>This is the main content area. Add your webpage content here.</p>
</main>

<footer>
    <p>© 2026 My Website | All Rights Reserved</p>
</footer>

</div>

</body>
</html>
