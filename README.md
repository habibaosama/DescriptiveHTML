# DescriptiveHTML
Building a language that parsed into html


the grammer of the language:

*create → "ADD" element
*element → img | header | para | url
*img → "IMAGE" "WITH" "SOURCE" quote sentence quote
*header → "HEADING" decorated_text
*para → "PARAGRAPH" decorated_text
*url → "LINK" decorated_url
*decorated_text → decorated_text "AND" decorated_text | text | color | font
*text → "WITH" "TEXT" quote sentence quote
*color → "WITH" "COLOR" quote sentence quote
*font → "WITH" "FONT" quote sentence quote
*sentence → sentence alphanumeric | 𝛆
*quote → "“"
*alphanumeric → "0"-"9" | "a"-"z" | "A"-"Z" | "/" | ":" | "."

For example:

-ADD IMAGE WITH SOURCE "https://www.w3schools.com/html/pic_trulli.jpg"
-ADD HEADING WITH TEXT "Hello World"
-ADD PARAGRAPH WITH TEXT "Welcome" AND WITH FONT "Arial" AND WITH COLOR "Red"
-ADD LINK WITH TEXT "Search" AND WITH LINK "http://google.com"

will convert to:

<img src="https://www.w3schools.com/html/pic_trulli.jpg" />
<h1>Hello World</h1>
<p style="color:Red;font-family:Arial;">Welcome</p>
<a href="http://google.com">Search</a>
