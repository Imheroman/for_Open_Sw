***
* # ***Linux Command***


## 1) **top**

top 명령어란? table of processes의 약자로  CPU와 메모리 이용에 관한 정보를 표시하는 수많은 유닉스 계열 운영 체제에서 볼 수 있는 작업 관리자 프로그램이며 시스템의 상태를 전반적으로 가장 빠르게 파악 가능(CPU, Memory, Process)하다.

top를 실행하는 동안에는 주기적인 업데이트로 실시간에 근접한 내용을 보여준다.

옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여주고, 서버정보, 프로세스 정보, CPU 정보, 메모리 정보 등을 나타내준다.

>top 실행하면서 줄 수 있는 옵션

|옵션|내용|
|:------:|:------:|
|-f|sort field 선택 화면 -> q 누르면 RES순으로 정렬|
|-a|메모리 사용량에 따라 정렬|
|-d 2(number)|2(number)초마다 정보 갱신|
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

ps란? process status의 줄인말로 현재 실행중인 프로세스 목록과 상태를 보여준다.(윈도우 작업관리자와 비슷한 일을 함)

어떤 OS 인지에 따라 명령어 사용법이 다름
System V : ps -ef
BSD ps aux를 입력하면 된다.


|명령어|내용|
|:---:|:---:|
|-e|모든(every) 프로세스, 현재 수행하고 있는 프로세스에 관한 정보 확인|
|-f|완전한(full) 포맷|
|-l|긴(long) 포맷|



## 3) **jobs**

jobs 명령어는 작업의 상태를 표시하는 명령어다.
현재 쉘 프로세스의 자식 백그라운드 프로세스들을 보여준다고 생각하면 된다.

현재 쉘 세션에서 실행시킨 백그라운드 작업의 목록이 출력되며, 각 작업에는 번호가 붙어 있어 kill 명령어 뒤에 ‘%번호’등으로 사용할 수 있다.


|명령어|내용|
|:---:|:---:|
|-l|프로세스 그룹 ID를 state 필드 앞에 출력|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
|-p|각 프로세스 ID에 대해 한 행씩 출력|
|command|지정한 명령어를 실행|



## 4) **kill**

|명령어|내용|
|:---:|:---:|
|-l|자세한 형태의 정보를 출력한다. |
|-u|각 프로세서의 사용자 이름과 시작 시간을 보여준다. |
|-j|작업 중심 형태로 출력한다.|
|-s|시그널 중심 형태로 출력한다.|
|-v|가상 메모리 중심 형태로 출력한다.|
|-m|메모리 정보를 출력한다. |
|-a|다른 사용자들의 프로세서도 보여준다.|
|-x|로그인 상태에 있는 동안 아직 완료되지 않은 프로세서들을 보여준다.|
|-S|차일드(child) CPU 시간과 메모리 페이지 결함(fault) 정보를 추가 한다.|
|-c|커널 task_structure로 부터 명령 이름을 보여준다.|
|-e|모든 프로세스를 보여줍니다.|
|-w|긴(wide) 형태로 출력한다. 한 행 안에 출력이 잘리지 않는다. |
|-h|헤더를 출력하지 않는다. |
|-r|현재 실행중인 프로세서를 보여준다.|
|-n|USER 와 WCHAN 을 위해 수치 출력을 지원한다.|
|-f|모든 정보를 출력합니다|


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
7. [about_ps3](https://shanepark.tistory.com/196 "ps2")
8. [about_jobs](https://hbase.tistory.com/265 "jobs")
9. [about_kill](https://121202.tistory.com/45 "kill")
10. [about_vim_macro](http://aboutmadlife.blogspot.com/2014/09/linux-vi-macro.html "macro")



