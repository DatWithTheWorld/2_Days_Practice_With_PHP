# 7_Days_Practice_With_PHP

<details>
<summary> <h1>PHP Syntax</h1> </summary>
-- Both type of 'echo' such as 'Echo,ECho,EcHo' can use similar.

-- The name of variable must true. Example: Color and COLOR are different value. 
</details>

<details>
<summary> <h2>How to get Data type ??</h2> </summary>
--Use var_dump($variable_name) function. This function will return the data type of this variable.
</details>

<details>
<summary> <h2>Define a constructor</h2> </summary>
  Access modifier _ function _ __construct(Some variable){}   ---- Contructor here is not same with Java. OOP PHP models
</details>

<details>
<summary> <h2>PHP String ?</h2> </summary>
 --Include somes function to work with string such as: <br>
    - strlen("String") : Return the length of this String <br>
    - str_word_count : To caculate the number of the word in the String <br>
    - strrev() : To reverse the String <br>
    - strpos("String","Character in this String"): return index of character where it start in the String <br>
    - str_replace("The word wanna to replace","New String","The first String") : To replace some word in a String;<br>
    - can concatenation two string by using dot (.) For example $txt1.$txt2
</details>
<details>
<summary> <h2>About PHP number </h2> </summary>
--When you define the number such as a number 80 and another one iss "80". It mean that you define the number with two type . 
First is integer and another one is String.
</details>
<details>
<summary> <h2>PHP Constant</h2> </summary>
-define(name, value, case-insensitive)
<br>
-To define an array

```php
<?php
define("cars", [
  "Alfa Romeo",
  "BMW",
  "Toyota"
]);
echo cars[0];
?>
```

</details>

<details>
<summary> <h2>PHP String ?</h2> </summary>
 --Include somes function to work with string such as: <br>
    - strlen("String") : Return the length of this String <br>
    - str_word_count : To caculate the number of the word in the String <br>
    - strrev() : To reverse the String <br>
    - strpos("String","Character in this String"): return index of character where it start in the String <br>
    - str_replace("The word wanna to replace","New String","The first String") : To replace some word in a String;<br>
    - can concatenation two string by using dot (.) For example $txt1.$txt2
</details>
<details>
<summary> <h2>PHP date and time </h2> </summary>
-- Use this function to set your country time 

``` php
date_default_timezone_set("America/New_York");
```

-- About define new time 

  ``` php
  mktime(hour, minute, second, month, day, year)
  ```

  -- Use this method to change type string of input to type date

  ```php

  strtotime(time, now)

  ```


</details>
<details>
<summary> <h2>PHP Inlude</h2> </summary>
 --Be like import. include can use to render code (same with iframe)
 --After call include in this file can apply css or many attribute.
</details>
<details>
<summary> <h2>PHP File Handling</h2> </summary>
 -- Use function readfile() to collect all information in file which is called
 
 ```php
 readfile("filename.type");
 
  ``` 
-- single function for file

  ```php
  fopen(),fclose(),fread(),
  
  fgets() -- read single line
  ```

  --check for file is end ?

  ```php
  feof()
  ```
  --different with fget() and fgetc()

  --fgetc() to read the single character

  --Use method fwrite() to write the content to file is called

  -- Some mode in file handling
  ```php
  -r - read only (pointer start at beginning of file)
  -w - write only (start at beginning)
  -a - write only (start at the end)
  -x - create new file for write only
  -r+ - read/write (pointer at the beginning)
  -w+ 
  -a+ - read/write (at the end)
  -x+ - create file for read/write
  
  ```


  -- Upload file --
  -- First is configure  -- configure file "php.ini" and then search for file_uploads and set it to on;

  --code

  ```php
  <?php
$target_dir = "uploads/";
$target_file = $target_dir . basename($_FILES["fileToUpload"]["name"]);
$uploadOk = 1;
$imageFileType = strtolower(pathinfo($target_file,PATHINFO_EXTENSION));
// Check if image file is a actual image or fake image
if(isset($_POST["submit"])) {
  $check = getimagesize($_FILES["fileToUpload"]["tmp_name"]);
  if($check !== false) {
    echo "File is an image - " . $check["mime"] . ".";
    $uploadOk = 1;
  } else {
    echo "File is not an image.";
    $uploadOk = 0;
  }
}
?>
  ```
  --explain
  ```php
  $target_dir = "uploads/" - specifies the directory where the file is going to be placed
$target_file specifies the path of the file to be uploaded
$uploadOk=1 is not used yet (will be used later)
$imageFileType holds the file extension of the file (in lower case)
Next, check if the image file is an actual image or a fake image
  ```

```php
// Check if file already exists
if (file_exists($target_file)) {
  echo "Sorry, file already exists.";
  $uploadOk = 0;
}
```
```php
// Check file size
if ($_FILES["fileToUpload"]["size"] > 500000) {
  echo "Sorry, your file is too large.";
  $uploadOk = 0;
}
```




</details>













