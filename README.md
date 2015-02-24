# BlogJS
[www.romellogoodman.com/blogjs](http://www.romellogoodman.com/blogjs "BlogJS' Homepage")

BlogJS A JSON Powered Blog System.

Documentation is a work in progress.

## Requirements
jQuery (for now)

### To use
``` HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Link to jQuery. -->
  <script src="jquery.min.js"></script>
  <!-- Link to your JSON object with all of your data. -->
  <script src="posts.js"></script>
  <!-- Link to BlogJS. -->
  <script src="BlogJS.js"></script>
  <script>
    // Set your initials
    window.onload = function(){
      // Set this field equal to your JSON object.
      BlogJS.initials.blogPosts = posts;
      // Specify the place where the posts load (defaulted to #posts)
      BlogJS.initials.appendListTo = "#list-of-articles";
      // Specify the place where the list of articles load (defaulted to #list-of-articles)
      BlogJS.initials.appendPostTo = "#post";
      // Specify the page where the #list-of-articles & #post are.
      // Both are defaulted to index. (index.html)
      BlogJS.initials.postLocation = "index";
      BlogJS.initials.listLocation = "index";
      // Starts the whole process.
      BlogJS.loadPage();
    };
  </script>
</head>
<body>
  <!-- Where the actual post will load -->
  <section id="post"></section>
  <!-- Where the list of articles will load -->
  <section id="list-of-articles"></section>
  <!-- Clicking will load the next 5 articles. -->
  <section id="load" onclick="BlogJS.loadArticleList(5)">
    <span><p class="center">Read More</p></span>
  </section>
</body>
</html>
```