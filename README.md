# krishsscodes.github.io-

<!DOCTYPE html>
<html>

<head>
  <title>Code Blocks with Syntax Highlighting and Copy</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.28.0/themes/prism-tomorrow.min.css">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    /* Custom CSS for black theme */

    body {
      background-color: #212121;
      color: #f5f5f5;
      font-family: Arial, sans-serif;
    }
/* Custom CSS for fixed navbar */
    .navbar {
    background-color: #333;
    color: #fff;
    padding: 20px;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 9999;
    }

    .navbar ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    }

    .navbar li {
    margin-right: 20px;
    }


    .navbar a {
      position: relative;
      color: #fff;
      text-decoration: none;
      padding-bottom: 4px;
    }
    
    .navbar a::after {
      content: "";
      position: absolute;
      bottom: 0;
      left: 50%;
      width: 0;
      height: 2px;
      background-color: #fff;
      transition: width 0.3s ease-in-out;
      transform: translateX(-50%);
    }
    
    .navbar a:hover::after {
      width: 100%;
      transition: width 0.3s ease-in-out;
    }
    pre {
      background-color: #212121;
      color: #f5f5f5;
      padding: 10px;
      border-radius: 5px;
      overflow: auto;
    }


    .no-right-click::after {
      content: "Right-click disabled";
      display: block;
      color: #fff;
      background-color: red;
      padding: 10px;
      font-size: 18px;
      text-align: center;
    }

    /* Optional CSS to style the copy buttons */
    button.copy {
      background-color: #212121;
      border: none;
      color: white;
      padding: 10px 20px;
      text-align: center;
      text-decoration: none;
      display: inline-block;
      font-size: 16px;
      margin: 4px 2px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    button.copy.copied {
      background-color: #2196F3;
      /* Blue */
    }

    button.copy::before {
      content: "\1F4CB";
      /* Unicode character for copy icon */
      margin-right: 5px;
    }


#scrollTopBtn {
  position: fixed;
  bottom: 20px;
  right: 20px;
  opacity: 0;
  transition: opacity 0.3s ease;
  background-color: #333;
  color: #fff;
  border: none;
  padding: 10px 15px;
  border-radius: 4px;
  cursor: pointer;
}

#scrollTopBtn:hover {
  background-color: #555;
}

#scrollTopBtn.visible {
  opacity: 1;
}



footer {
  background-color: #222;
  color: #fff;
  padding: 20px;
  text-align: center;
  font-family: monospace;
}

.footer-content {
  font-size: 14px;
  opacity: 0.8;
}

.footer-content::before,
.footer-content::after {
  content: "";
  display: block;
  height: 1px;
  background-color: #fff;
  margin: 10px 0;
}

.footer-content::before {
  width: 50px;
  margin-right: 10px;
  display: inline-block;
  vertical-align: middle;
}

.footer-content::after {
  width: 50px;
  margin-left: 10px;
  display: inline-block;
  vertical-align: middle;
}
  </style>
</head>

<body>
<nav class="navbar">
  <ul id="navbarItems">
    <li><a href="#section1">Section 1</a></li>
    <li><a href="#section2">Section 2</a></li>
    <li><a href="#section3">Section 3</a></li>
  </ul>
</nav>

<!-- Rest of your HTML code -->
<!-- ... -->


    
<h1>Let's learn Types of String Formatting</h1>


  <h3>Normal String Format</h3>
  <pre>
    <code class="language-python">
  >>> name1 = "Krishna"
  >>> name2 = "Ranveer"
  >>> name3 = "Hrithik"
  >>> print("Hey! ",name1, "Where is ",name2," and ", name3,"?")
    # Hey!  Krishna Where is  Ranveer and  Hrithik?
    </code>
    <button class="copy" onclick="copyCode(this)">Copy</button>
  </pre>

  <h3> Old-string formatting (% Oprator)</h3>
  <pre>
    <code class="language-python">
  >>> name1 = "Krishna"
  >>> name2 = "Ranveer"
  >>> name3 = "Hrithik"
  >>> print("Hey! %s Where is %s and %s?" % (name1, name2, name3))
    # Hey!  Krishna Where is  Ranveer and  Hrithik?
    </code>
    <button class="copy" onclick="copyCode(this)">Copy</button>
  </pre>
<p><a href="https://docs.python.org/3/library/string.html" style="color: #f5f5f5" target="_blank" onclick="openNewWindow(event)">Learn more about Old-string Formatting</a></p>


  <h3> New-string formatting (f Oprator)</h3>

  <pre>
    <code class="language-python">
  >>> name1 = "Krishna"
  >>> name2 = "Ranveer"
  >>> name3 = "Hrithik"
  >>> print(f"Hey! {name1} Where is {name2} and {name3}?")
    # Hey!  Krishna Where is  Ranveer and  Hrithik?
    </code>
    <button class="copy" onclick="copyCode(this)">Copy</button>
  </pre>

<button id="scrollTopBtn">Scroll to Top</button>


<script>
    
</script>

<footer>
    <div class="footer-content"> 
        All rights reserved &copy; Krishss Codes 
    </div> 
</footer>

<!-- End of code -->


  <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.28.0/prism.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.28.0/components/prism-python.min.js"></script>
  <script>
    function copyCode(element) {
      const code = element.previousElementSibling;
      const range = document.createRange();
      range.selectNode(code);
      window.getSelection().removeAllRanges();
      window.getSelection().addRange(range);
      document.execCommand('copy');
      window.getSelection().removeAllRanges();

      element.textContent = 'Copied';
      element.classList.add('copied');

      setTimeout(function () {
        element.textContent = 'Copy';
        element.classList.remove('copied');
      }, 10000); // 10 seconds
    }

    const scrollTopBtn = document.getElementById('scrollTopBtn');
    
    window.addEventListener('scroll', () => {
      scrollTopBtn.classList.toggle('visible', window.scrollY > 100);
    });
    
    scrollTopBtn.addEventListener('click', () => {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    });

    // window.addEventListener('contextmenu', function(e) {
    //   e.preventDefault();
    // });
</script>

<script>
    function openNewWindow(event) {
        event.preventDefault();
        window.open(event.target.href, '_blank', 'width=800,height=600,top=100,left=100');
    }
</script>
    



</body>

</html>
