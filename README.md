# Week-7-8
> Time taken to complete the lab and the assignment: 4 hrs.

## Lab Demo:
  * Title: WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
  * Fixed in: 4.2.10
  * procedure:
    * When an image with a file name such as ```cengizhansahinsumofpwn<img src=a onerror=alert(document.cookie)>.jpg``` is uploaded and         viewed within WordPress the script code is executed:
    
    ![picture alt](https://github.com/samuely4/Facebook-CodePath-CyberSecurity-Week-7-8-master/blob/master/Lab%20Demo%20pic%201.png "Lab Demo")
    
    * When viewing the attachment page, the exploit succeeded
    
    ![picture alt](https://github.com/samuely4/Facebook-CodePath-CyberSecurity-Week-7-8-master/blob/master/Lab%20Demo%20pic%203.PNG "Title is optional")
    
 ## Assignment Report:
 1. Authenticated Cross-Site Scripting (XSS) via Media File Metadata:
- [x] Problem Summary
  * Vulnerability types: XSS
  * Tested in version: 4.1.1
  * Fixed in version: 4.1.16
       
- [x] GIF Walkthrough
  ![picture alt](https://github.com/samuely4/Facebook-CodePath-CyberSecurity-Week-7-8-master/blob/master/xss2.gif "Assignment-xss1")
       
       
- [x] Brief Overview to recreate the exploit
 * Logged in as an admin, we attempted to upload an image. This version of Wordpress fails to sanitize filenames, so malicous javascript      can be injected into the filename. In this particular example, the file name was ```beauty_HACKED!!! <img src= a                          onerror=alert('HACKED!!!!!')>.jpg```. Upon viewing the attachement page of the image, the exploit succeeds.
       
       
- [x] Source Code
 * [Link to source code](https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7 "Link to source code")
 
 2. Wordpress: CVE-2017-9061: Cross-Site Scripting (XSS):
- [x] Problem Summary
  * Vulnerability types: XSS
  * Tested in version: 4.7.4
  * Fixed in version: 4.7.5
       
- [x] GIF Walkthrough
  ![picture alt](https://github.com/samuely4/Facebook-CodePath-CyberSecurity-Week-7-8-master/blob/master/xss3.gif "Assignment-xss2")
       
       
- [x] Brief Overview to recreate the exploit
 * Create a file that is larger than 2 MB. On Kali Linux operating system, we can easily do that through the following command: ```truncate -s 3M test.jpg```. This will create a 3 MB file named test.jpg. Rename the file with the intended Javascript code to be presented on error. i.e. ```Test<img src= a onerror=alert('Hacked!!!!!')>.jpg```
       
       
- [x] WordPress Security and Maintenance Release
 * [Security and Maintenance Release -- Securiyt Issue 5](https://wordpress.org/news/2017/05/wordpress-4-7-5/ "Assignment-xss2")
 

 3. Authenticated Stored Cross-Site Scripting (XSS):
- [x] Problem Summary
  * Vulnerability types: XSS
  * Tested in version: 4.5.3
  * Fixed in version: 4.6.1
       
- [x] GIF Walkthrough
  ![picture alt](https://github.com/samuely4/Facebook-CodePath-CyberSecurity-Week-7-8-master/blob/master/xss1.gif "Assignment-xss3")
       
       
- [x] Brief Overview to recreate the exploit
 * Log in as a registered user and create a new post. Using the editior, you can inject malicious content into your blog post title. i.e. ```<a href="></a><a title=" onmouseover=alert('Hacked!!!!!') "> link</a>```
       
       
- [x] Source Code
 * [Link to source code](https://core.trac.wordpress.org/changeset/33359 "Link to source code")
 
 4. Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds:
- [x] Problem Summary
  * Vulnerability types: XSS
  * Tested in version: 4.1.1
  * Fixed in version: 4.1.16
       
- [x] GIF Walkthrough
  ![picture alt](https://github.com/samuely4/Facebook-CodePath-CyberSecurity-Week-7-8-master/blob/master/xss4.gif "Assignment-xss4")
       
       
- [x] Brief Overview to recreate the exploit
 * Log in as a registered user and create a post. Using the editor, embed a YouTube video and inject your Javascript code to have a      stored XSS attack. i.e. ```[embed src='https://www.youtube.com/embed/abcd\x3csvg onload=alert("Hacked..Hacked..haha")\x3e'][/embed]```
       
       
- [x] Source Code
 * [Link to source code](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8 "Link to source code")
 
 
 # Resources Used in Lab/Assignment:
 * Kali Linux OS
 * VirtualBox
 * WordPress 4.2
 * WPScan
 * LICEcap to create the GIFs
 
 # Note
 * Materials used to do this lab are to be found in the repository
 
 
 

