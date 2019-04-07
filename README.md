# Project7
Project #7 Codepath Spring 2019
# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID: Exploit #1 (XSS w/ a Link in Title)
  - [x] Summary: Able to add XSS within hyperlinks when creating the title of a post, activates when hovering mouse over link.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.4
  - [x] GIF Walkthrough: [Here](https://github.com/ShelbyMitchell/Project7/blob/master/Exploit%231XSS.gif)
  - [x] Steps to recreate: 
    - Go to posts and create a new post
    - Enter (w/ tags) into title slot: a href= " " onmouseover= "alert('XSS!');>CLICK THIS LINK< /a
    - Click to view the post, and as you hover your mouse over the title, an alert will pop up that reads "XSS!"
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Vulnerability Name or ID: Exploit #2 (XSS w/ Hidden Link in Image)
  - [x] Summary: Able to add XSS within an image tag that activates when the mouse is hovering over it.
    - Vulnerability types: XSS
    - Tested in version: 4.2 
    - Fixed in version: 4.6
  - [x] GIF Walkthrough: [Here](https://github.com/ShelbyMitchell/Project7/blob/master/Exploit%232XSSImage.gif)
  - [x] Steps to recreate: 
     - Go to posts and create a new post
     - Enter in an image tag w/ text
     - In between 'alt = "..."' and 'width = ""', enter in: onmouseover="alert('XSS Attack!')"
     - Click to view post, and as you hover your mouse over the image, an alert will pop up that reads "XSS Attack!"
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Vulnerability Name or ID: Exploit #3 (XSS in Comment Section)
  - [x] Summary: Able to add XSS in the comment section, so whenever that post's page is refreshed or uploaded, an XSS alert pops up.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.4
  - [x] GIF Walkthrough: [Here](https://github.com/ShelbyMitchell/Project7/blob/master/Exploit%233XSSComment.gif)
  - [x] Steps to recreate: 
    - Scroll down to comment section and click to add a comment
    - In comment text box type in: <script>alert('XSScommentattack')</script>
    - Upload the comment, afterwards, whenever that page is accessed or refreshed, an alert will pop up that reads "XSS Comment Attack!"
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
