***
* # ***Linux Command***


## 1) **top**

>***사용법 : top [option]***

top 명령어란? table of processes의 약자로  CPU와 메모리 이용에 관한 정보를 표시하는 수많은 유닉스 계열 운영 체제에서 볼 수 있는 작업 관리자 프로그램이며 시스템의 상태를 전반적으로 가장 빠르게 파악 가능(CPU, Memory, Process)하다.

top를 실행하는 동안에는 주기적인 업데이트로 실시간에 근접한 내용을 보여준다.

옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여주고, 서버정보, 프로세스 정보, CPU 정보, 메모리 정보 등을 나타내준다.

>top 실행하면서 줄 수 있는 옵션

|명령어|내용|
|:------:|:------:|
|-f|sort field 선택 화면 -> q 누르면 RES순으로 정렬|
|-a|메모리 사용량에 따라 정렬|
|-d 2(number)|2(number)초마다 정보 갱신|
|-p|특정 PID 값을 갖는 프로세스를 모니터링할 때 사용|
|-c|명령어 대신 명령어 라인을 보여줌
|-n|반복의 최대 수를 결정|
|-1|CPU Core별로 사용량 보여줌|
|-b|Batch 모드로 작동|
|-s|보안모드로 시작|

>top 실행 후 명령어

|명령어|내용|
|:---:|:---:|
|k|kill 명령|
|r|nice |
|space bar|현재 화면 갱신|
|O|화면 정렬 기준 지정|
|B|글씨를 두껍게|
|u|사용자에 따른 정렬|
|q|top 종료|
|shift + p|CPU 사용률 내림차순|
|shit + m|메모리 사용률 내림차순|
|shift + t|프로세스가 돌아가고 있는 시간 순|

* *ps와 top의 차이점*: **ps**는 ps한 시점에 proc에서 검색한 cpu 사용량이고, **top**은 proc에서 일정 주기로 합산해 cpu 사용율을 출력한다.

## 2) **ps**

>***사용법 : ps [option]***

ps 란? process status의 줄인말로 현재 실행중인 프로세스 목록과 상태를 보여준다. ps 명령어는 어떤 OS 인지에 따라 명령어 사용법이 다르다.(윈도우 작업관리자와 비슷한 일을 함)

>OS에 따른 ps 명령어

|OS|명령어|
|:---:|:---:|
|System V 계열|옵션 사용할 때 - 사용|
|BSD 계열|옵션 사용할 때 - 사용안 함|
|GNU 계열|옵션 사용할 때 --(2개) 사용|
|System V 계열|ps -ef (옵션 사용할 때 - 사용)|
|BSD 계열|ps aux (옵션 사용할 때 - 사용안 함)|

>ps 실행할 때 줄 수 있는 옵션

|명령어|내용|
|:---:|:---:|
|-A|모든 프로세스를 출력|
|-a|터미널에 종속되지 않은 모든 프로세스 출력|
|-r|현재 실행중인 프로세서를 출력|
|-e|모든(every) 프로세스(커널 프로세스를 제외한 모든 프로세스를 출력)|
|-f|완전한(full) 포맷(유닉스 스타일로 출력하는 옵션)|
|-l|긴(long) 포맷|

>ps 실행시 나타나는 항목

|항목|의미|
|:---:|:---:|
|USER|BSD 계열에서 나타나는 항목으로 프로세스 소유자의 이름|
|UID|SYSTEM V 계열에서 나타나는 항목으로 프로세스 소유자의 이름|
|PID|프로세스의 식별번호|
|PPID|부모 프로세스 ID|
|%CPU|CPU 사용 비율의 추정치(BSD)|
|%MEM|메모리 사용 비율의 추정치(BSD)|
|VSZ|K단위 또는 페이지 단위의 가상메모리 사용량|
|RSS|실제 메모리 사용량 (Resident Set Size)|
|TTY|프로세스와 연결된 터미널|



## 3) **jobs**

>***사용법 : jobs [option]***

jobs 명령어는 백그라운드로 실행중인 프로세스와 현재 중지된 프로세스의 목록을 출력해주는 명령어다.

현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력되며, 각 작업에는 번호가 붙어 있어 kill 명령어 뒤에 ‘%번호’등으로 사용할 수 있다.

>jobs 실행할 때 줄 수 있는 옵션

|명령어|내용|
|:---:|:---:|
|-l|프로세스 번호(PID)를 추가로 출력|
|-n|상태변화를 일으킨 |
|-p|해당 작업의 대표 프로세스의 ID만 출력|
|command|지정한 명령어를 실행|



## 4) **kill**

>***사용법 : kill [option]  [signal]***

kill 명령어란? 프로세스에 특정한 시그널을 보내는 명령어로 보통 중지시킬 수 없는 프로세스를 종료시킬 때 사용한다.

>kill 실행할 때 줄 수 있는 옵션

시그널은 1~31까지 있다.

|명령어|내용|
|:---:|:---:|
|-l|사용 가능한 시그널 목록을 출력|
|-1|재실행|
|-9|강제종료|
|-15|정상종료|
|-19|즉각 정지|
|-u|각 프로세서의 사용자 이름과 시작 시간을 보여준다.|
|-j|작업 중심 형태로 출력한다.|
|-s|시그널 중심 형태로 출력한다.|

---


+ # ***Vim Command***

## 1. **매크로(q)**

매크로란? 특정한 움직임 또는 입력을 키에 저장함으로써 단순하면서 반복되는 동작을 쉽고 빠르게 해주는 것을 말한다.
vim에서 매크로는 명령어 모드에서 q + 알파벳 을 눌러 특정 알파벳에 매크로를 저장할 수 있다.

|명령어|내용|
|:---:|:---:|
|q + a |입력된 알파벳(a)를 단축키로 매크로 시작|
|q|매크로 종료|
|@ + a|저장된 매크로 실행|
|5(number) + @ + a|5(number) 횟수만큼 매크로 실행|
|@@|방금 실행했던 매크로 실행|

***

- #  ***참고 사이트, 출처***

1. [about_top](https://sabarada.tistory.com/146 "top")
2. [about_top2](https://zzsza.github.io/development/2018/07/18/linux-top/ "top2")
3. [about_top3](https://cheershennah.tistory.com/172 "top3")
4. [about_top4](https://m.blog.naver.com/minki0127/220773217082 "top4")
5. [about_top5](https://m.blog.naver.com/hanajava/220988767444 "top5")
6. [about_ps](https://newstars.cloud/468 "ps")
7. [about_ps2](https://jhnyang.tistory.com/268 "ps2")
8. [about_ps3](https://shanepark.tistory.com/196 "ps3")
9. [about_jobs](https://hbase.tistory.com/265 "jobs")
10. [about_jobs2](https://starrykss.tistory.com/1694 "jobs2")
11. [about_jobs3](https://blog.naver.com/PostView.nhn?isHttpsRedirect=true&blogId=errorsoft666&logNo=221502257635&parentCategoryNo=&categoryNo=1&viewDate=&isShowPopularPosts=false&from=postView "jobs3")
12. [about_kill](https://121202.tistory.com/45 "kill")
13. [about_kill](https://starrykss.tistory.com/1692?category=592475 "kill2")
14. [about_vim_macro](http://aboutmadlife.blogspot.com/2014/09/linux-vi-macro.html "macro")
15. [many](https://chancoding.tistory.com/164)



