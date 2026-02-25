<!DOCTYPE html>
<html>
<head>
    <title>E-Library Home</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1>📚 Welcome to My E-Library</h1>
    <p>Online Books पढ़ें और Download करें</p>

    <a href="books.html" class="btn">View Books</a>

</body>
</html>
<div class="book-container" id="bookList">

    <div class="book">
        <h3>HTML Basics</h3>
        <p>Beginner friendly HTML guide.</p>
        <a href="#" class="btn">Download</a>
    </div>

    <div class="book">
        <h3>CSS Mastery</h3>
        <p>Complete CSS styling course.</p>
        <a href="#" class="btn">Download</a>
    </div>

    <div class="book">
        <h3>JavaScript Guide</h3>
        <p>Learn JS step by step.</p>
        <a href="#" class="btn">Download</a>
    </div>

    <div class="book">
        <h3>Python Programming</h3>
        <p>Python from basic to advance.</p>
        <a href="#" class="btn">Download</a>
    </div>

</div>

<footer>
    <p>© 2026 My E-Library | Developed by Vijay</p>
</footer>

<script src="script.js"></script>
<!DOCTYPE html>
<html>
<head>
    <title>Books - E-Library</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<h1>Available Books</h1>

<div class="book">
    <h3>HTML Guide</h3>
    <a href="#">Read</a>
</div>

<div class="book">
    <h3>CSS Basics</h3>
    <a href="#">Read</a>
</div>

<div class="book">
    <h3>JavaScript Intro</h3>
    <a href="#">Read</a>
</div>

<br>
<a href="index.html" class="btn">Back to Home</a>

</body>
</html>
</body>
</html>
body {
    margin: 0;
    font-family: Arial;
    background: #f4f6f9;
    text-align: center;
}

header {
    background: #1e3c72;
    color: white;
    padding: 20px;
}

.search-box {
    margin: 20px;
}

.search-box input {
    padding: 10px;
    width: 60%;
    max-width: 400px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.book-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.book {
    background: white;
    width: 250px;
    margin: 15px;
    padding: 15px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.book h3 {
    margin: 10px 0;
}

.btn {
    display: inline-block;
    padding: 8px 15px;
    background: #1e3c72;
    color: white;
    text-decoration: none;
    border-radius: 5px;
}

.btn:hover {
    background: #16305c;
}

footer {
    margin-top: 30px;
    padding: 15px;
    background: #1e3c72;
    color: white;
}
body {
    font-family: Arial;
    text-align: center;
    background-color: #f2f2f2;
}

h1 {
    color: darkblue;
}

.book {
    background: white;
    margin: 15px auto;
    padding: 15px;
    width: 250px;
    border-radius: 8px;
    box-shadow: 0px 0px 5px gray;
}

a {
    text-decoration: none;
    color: white;
    background: blue;
    padding: 8px 15px;
    border-radius: 5px;
}

.btn {
    display: inline-block;
    margin-top: 20px;
}
function searchBooks() {
    let input = document.getElementById("searchInput").value.toLowerCase();
    let books = document.getElementsByClassName("book");

    for (let i = 0; i < books.length; i++) {
        let title = books[i].getElementsByTagName("h3")[0];
        if (title.innerHTML.toLowerCase().indexOf(input) > -1) {
            books[i].style.display = "";
        } else {
            books[i].style.display = "none";
        }
    }
}
