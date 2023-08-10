---
title: "hugo로 블로그 만들기"  
date: 2023-08-10T10:43:40+09:00
published: true
---

 ## hugo로 블로그 만들기- 드디어 만들었다 :baby_chick: 
 ***
 ### error1

 어제 계속 시도했었는데  
 bo-ram-bo-ram.github.io 레포랑 연결하는 부분에서  계속 오류가 났다  
 해결하고 난 다음 지금 생각해보면 폴더 구조를 잘못만들었던 것 같다  
 Blog 폴더 안에서bo-ram-bo-ram.github.io 폴더를 만들어서 진행했더니  
 자꾸 **fatal: 'public' does not have a commit checked out**  
 오류가 떴는데 이게 이미 git 파일이 있을 때 나오는 오류라고 한다  
 git을 임의로 지우니 또 에러가 뜨고 다시 생성되기를 반복했다!  
 이미 Blog 레포랑 연결을 했던 폴더에서 진행해서 그런것이었다  

 이 [영상](https://youtu.be/LIFvgrRxdt4)  참고해서 만드니까 잘 만들어졌다  

 ***

 ### error2
 다 만들고 났더니 테마가 적용이 안되는 오류가 났다  
 블로그에서 개발자 도구를 열어보니  
  
 **Mixed Content: The page at 'https://bo-ram-bo-ram.github.io/' was loaded over HTTPS, but requested an insecure stylesheet 'http://bo-ram-bo-ram.github.io/main.min.css'. This request has been blocked; the content must be served over HTTPS.**  
 에러였는데내가이게 http랑 https랑 혼합돼서 나오는 에러였다  
 모든 파일을 열어볼 생각에 아찔햇는데 혹시 몰라서 baseURL을 확인해봤더니 내가 레포링크를 http로 적어놨었다  
 다행히 그 링크만 https로 바꿨더니 테마가 잘 적용됐다!  
 아마 유튜브 영상은 2021영상이었는데 최근 보안이슈로 http가 막힌 것 같다  

 ***

 ### error3
 이모지쓰고싶어서 계속 이것저것 했는데 그냥 출력되는 것이다!  
 이모티콘 마저 맘대로 쓸 수 없다니뭐가 문제인가하고 찾아보니까  
 hugo.toml에서 **enableEmoji=true**를 했어야했다  
 아캔두

 *** 

 ### error4
 이모지를 넣고싶어서 계속 이 파일을 만지작 거렸더니 갑자기 **assemble: "E:\study\Blog\boram_blog\content\posts\mypost.md:1:1": failed to unmarshal YAML: yaml: line 2: mapping values are not allowed in this contex** 이런 에러가 떴다  
 알고보니 맨 첫줄 ---뒤에 공백이 들어가있었고 들여쓰기가 문제였다..  
 그렇다.. 공백 주의하자!  


 ***
 ### 테마 커스텀  
 사람의 욕심은 끝이 없었다  
 블로그를 5-6시간 만에 만들어놓고 테마를 커스텀 하고싶어졌다  
 ㅋㅋㅋㅋㅋutterances로 댓글 구현하고싶었는데...  
 도저히 어디 html에 붙여넣어야하는지 못찾았다  
 이건 다음에 해봐야지  
 기록용으로 붙여놓을 소스 남겨놓는다!  

 ```
 <script src="https://utteranc.es/client.js"
        repo="bo-ram-bo-ram/blog_comment"
        issue-term="title"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
 ```

 tmi 1 ) 달 눌러보세요
 tmi 2 ) [이모지](https://www.webfx.com/tools/emoji-cheat-sheet/) 최고 :heart:

