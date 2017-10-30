# Project 7 - WordPress Pentesting

Time spent: **12** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID
  - [ ] Summary: Unauthenticated Stored Cross-Site Scripting (XSS)
    - Vulnerability types:XSS
    - Tested in version:4.0
    - Fixed in version:4.1.2 
  - [ ] GIF Walkthrough: 
  
  
  - [ ] Steps to recreate: 
    GO to create a new post and view new post, and uder this post insert code on the commend.
  - [ ] Affected source code:
    - [Link 1](https://cedricvb.be/post/wordpress-stored-xss-vulnerability-4-1-2/)
1. (Required) Vulnerability Name or ID
  - [ ] Summary: 3.7-4.4.1 - Local URIs Server Side Request Forgery (SSRF)
    - Vulnerability types:SSRF
    - Tested in version:4.0
    - Fixed in version: 4.0.10
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
    
    Victim is logged into Wordpress.
    Victim visits bad site with a content of`<img src="//myWordpress.com/wp-admin/press-this.php?u=htto://0.0.0.0:8080&url-scan-submit=Scan" />
    Victim sends a unwanted request to their server requesting a internal server address to be hit.
    Server sends get request to 0.0.0.0:8080
    Servers private 127.0.0.1 answers back.

  - [ ] Affected source code:
    - [Link 1](https://hackerone.com/reports/110801)
1. (Required) Vulnerability Name or ID 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
  - [ ] Summary: 
    - Vulnerability types:Cross-Site Scripting
    - Tested in version:4.0
    - Fixed in version: 4.0.13
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
      add a new post
      insert a image with file name cengizhansahinsumofpwn<img src=a onerror=alert(document.cookie)>.jpg
  - [ ] Affected source code:
    - [Link 1](https://sumofpwn.nl/advisory/2016/persistent_cross_site_scripting_vulnerability_in_wordpress_due_to_unsafe_processing_of_file_names.html)
    
1. (Required) Vulnerability Name or ID 4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.0
    - Fixed in version: 4.0.16
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate:
      create a new post with format video
      insert https://youtube[.]com/watch?v=abc<svg onload=alert(1)> on the context
      pubnish and view post
  - [ ] Affected source code:
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
