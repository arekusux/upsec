# Application layer DoS
Main info:
* [Denial of Service Cheat Sheet](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Denial_of_Service_Cheat_Sheet.md)
* [Defending against application DoS](https://owasp.org/www-pdf-archive/Roberto_Suggi_Liverani_OWASPNZDAY2010-Defending_against_application_DoS.pdf)

General scaners:
* [FindSecBug](https://find-sec-bugs.github.io)
* [AFL](https://github.com/google/AFL)
* [AFL for Java](https://github.com/Barro/java-afl)
* 

## Regular expression Denial of Service - ReDoS
Information:
* https://owasp.org/www-community/attacks/Regular_expression_Denial_of_Service_-_ReDoS
* https://checkmarx.com/wp-content/uploads/2015/03/ReDoS-Attacks.pdf
* https://checkmarx.com/blog/redos-go/
* https://www.usenix.org/system/files/sec21-li-yeting.pdf

Cases:
* https://segment.com/docs/release_notes/2021-07-13-cve-2021-36716/
* https://security.netapp.com/advisory/ntap-20210702-0007/
* https://www.openwall.com/lists/oss-security/2021/08/18/1
* https://github.com/PrismJS/prism/security/advisories/GHSA-gj77-59wh-66hg
* https://ckeditor.com/blog/CKEditor-4.16-with-improved-image-pasting-High-Contrast-support-and-a-new-color-API/#security-comes-first

Tools:
* https://github.com/NicolaasWeideman/RegexStaticAnalysis

## Cache Poisoned Denial of Service
Information:
* https://cpdos.org
* https://habr.com/ru/post/492718/
* https://portswigger.net/research/responsible-denial-of-service-with-web-cache-poisoning

Cases:
* https://hackerone.com/reports/622122
* https://portswigger.net/research/responsible-denial-of-service-with-web-cache-poisoning

## Markup Language Denial of Service
Information:
* [XML_External_Entity_DOS](https://www.ws-attacks.org/index.php/XML_External_Entity_DOS)
* [XML Security Cheat Sheet](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/XML_Security_Cheat_Sheet.md)
* [XML External Entity Prevention Cheat Sheet](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/XML_External_Entity_Prevention_Cheat_Sheet.md)

Cases:
* https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-11462
* http://poi.apache.org/#20+March+2017+-+CVE-2017-5644+-+Possible+DOS+%28Denial+of+Service%29+in+Apache+POI+versions+prior+to+3.15
* https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-5644
* https://github.com/kubernetes/kubernetes/issues/89535
* [XXE Injection through SVG image upload](https://hackerone.com/reports/897244)
* https://hackerone.com/reports/36450
* https://hackerone.com/reports/409701

Tools:
* https://github.com/ssexxe/XXEBugFind

## Client-side resource starvation
Cases:
* [Pixel flood attack](https://hackerone.com/reports/126826)
* [DoS on the Issue page by exploiting Mermaid](https://hackerone.com/reports/470067)
* https://hackerone.com/reports/768677
* https://hackerone.com/reports/993005
* https://hackerone.com/reports/764434

## Server-side memory starvation
Cases:
* [Pixel flood attack](https://hackerone.com/reports/126826)
* https://labs.sentinelone.com/hotcobalt-new-cobalt-strike-dos-vulnerability-that-lets-you-halt-operations/
* [zTXt Compressed textual data](https://hackerone.com/reports/454)
* https://baraktawily.blogspot.com/2018/02/how-to-dos-29-of-world-wide-websites.html

## Prototype Pollution
Information:
* [JavaScript prototype pollution: практика поиска и эксплуатации](https://habr.com/ru/company/huawei/blog/547178/)

Cases:
* [Mermaid Prototype Pollution vulnerability](https://hackerone.com/reports/1106238)
* https://hackerone.com/reports/968355
* https://hackerone.com/reports/871156
* https://hackerone.com/reports/350418

## Cryptography and Big Numbers
Cases:
* https://hackerone.com/reports/479144
* https://symfony.com/blog/security-releases-cve-2013-5958-symfony-2-0-25-2-1-13-2-2-9-and-2-3-6-released
* https://phabricator.wikimedia.org/T64685

## User influence on the complexity of the work
Cases:
* https://github.com/charleskorn/kaml/security/advisories/GHSA-fmm9-3gv8-58f4
* https://github.com/jhy/jsoup/security/advisories/GHSA-m72m-mhq2-9p6c
* https://hackerone.com/reports/361337
* https://hackerone.com/reports/136221
* https://hackerone.com/reports/500686

Tools:
* https://github.com/CodeIntelligenceTesting/jazzer

## Enternal Services
Information:
* [Google Api security best practices](https://developers.google.com/maps/api-security-best-practices)

Cases:
* https://hackerone.com/reports/1093667
* https://hackerone.com/reports/1065041
* https://hackerone.com/reports/823915

## Memory Management
Information:
* https://en.wikipedia.org/wiki/Buffer_overflow
* https://wiki.sei.cmu.edu/confluence/pages/viewpage.action?pageId=87151930

Cases:
* https://github.com/mrash/afl-cve

Tools:
* https://github.com/google/AFL
