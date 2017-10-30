# Project 7 - WordPress Pentesting

Time spent: **12** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID Unauthenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.0
    - Fixed in version:4.1.2 
  - [X] GIF Walkthrough: 
  ![cxx2](https://user-images.githubusercontent.com/21352483/32157258-c828aac8-bd18-11e7-98f8-95bfca270e1c.gif)
  - [X] Steps to recreate: 
    - GO to create a new post and view new post, and uder this post insert code on the commend.
  - [X] Affected source code:
    - [Link 1](https://cedricvb.be/post/wordpress-stored-xss-vulnerability-4-1-2/)
1. (Required) Vulnerability Name or ID 3.7-4.4.1 - Local URIs Server Side Request Forgery (SSRF)
  - [X] Summary: 
    - Vulnerability types:SSRF
    - Tested in version:4.0
    - Fixed in version: 4.0.10
  - [X] GIF Walkthrough: 
  ![3](https://user-images.githubusercontent.com/21352483/32157144-0cdef54c-bd18-11e7-9133-6a96a2ab57a1.gif)
  - [X] Steps to recreate: 
    - Victim is logged into Wordpress.
    - Victim sends a unwanted request to their server requesting a internal server address to be hit.
    - Server sends get request to 0.0.0.0:8080
  - [X] Affected source code:
    - [Link 1](https://hackerone.com/reports/110801)
1. (Required) Vulnerability Name or ID 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
  - [X] Summary: 
    - Vulnerability types:Cross-Site Scripting
    - Tested in version:4.0
    - Fixed in version: 4.0.13
  - [X] GIF Walkthrough:
    ![image](https://user-images.githubusercontent.com/21352483/32157093-a22ea1d4-bd17-11e7-8032-0365992474e7.gif)
  - [X] Steps to recreate: 
      add a new post
      insert a image with file name cengizhansahinsumofpwn<img src=a onerror=alert(document.cookie)>.jpg
  - [X] Affected source code:
    - [Link 1](https://sumofpwn.nl/advisory/2016/persistent_cross_site_scripting_vulnerability_in_wordpress_due_to_unsafe_processing_of_file_names.html)
    
1. (Required) Vulnerability Name or ID 4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [X] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.0
    - Fixed in version: 4.0.16
  - [X] GIF Walkthrough:
  ![youtube](https://user-images.githubusercontent.com/21352483/32157259-cac53f94-bd18-11e7-8ae4-c69b3d45e5c3.gif)
  - [X] Steps to recreate:
      create a new post with format video
      insert https://youtube[.]com/watch?v=abc<svg onload=alert(1)> on the context
      pubnish and view post
  - [X] Affected source code:
    - [Link 1](https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2017] [Aijie Chen]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
