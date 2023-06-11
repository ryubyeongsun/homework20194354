# homework 20194354 류병선


# 명령어 목록


1. [top](https://terms.naver.com/entry.naver?docId=4125861&cid=59321&categoryId=59321 "top 명령어설명")
2. [ps](https://terms.naver.com/entry.naver?docId=4125773&cid=59321&categoryId=59321 "ps 명령어설명")
3. [jobs](https://terms.naver.com/entry.naver?docId=4125682&cid=59321&categoryId=59321 "jobs 명령어설명")
4. [kill](https://terms.naver.com/entry.naver?docId=4125687&cid=59321&categoryId=59321 "kill 명령어설명")

## top 명령어

`top` 명령어는 리눅스에서 실행 중인 프로세스의 실시간 시스템 모니터링을 제공하는 유틸리티입니다.
### top 명령어 옵션(top 실행중 사용가능)

실행 중 누르면 확인이 가능한 옵션이 있음. 따라서 들어가서 확인이 필요합니다.

shift + p : CPU 사용률이 높은 프로세스 순서대로 표시

shift + m : 메모리 사용률이 높은 프로세스 순서대로 표시

shift + t : 프로세스가 돌아가고 있는 시간 순서대로 표시

k : 프로세스  kill  - k 입력 후 종료할 PID 입력 signal을 입력하라고 하면 kill signal인 9를 입력

a : 메모리 사용량에 따라 정렬

b : Batch 모드 작동

c : 명령행/프로그램 이름 토글

d : 지연 시간 간격은 다음과 같다. -d ss. tt (seconds.tenths)

h : 도움말 

H : 스레드 토글

i : 유휴 프로세스 토글

m : VIRT/USED 토글

M : 메모리 유닛 탐지

n : 반복 횟수 제한 : -n number

p : PID를 다음과 같이 모니터 : -pN1 -pN2 ... or -pN1, N2 [, ...] 

s : 보안 모드 작동

S : 누적 시간 모드 토글

u : 사용자별 모니터링 : u somebody

U : 사용자별 모니터링 : U somebody

u : 입력한 유저의 프로세스만 표시  which u

숫자 1 : CPU Core별로 사용량을 보여줍니다.

![top 명령어 실행 예시](https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2FMjAyMzA0MjVfMjY4%2FMDAxNjgyNDAxMTUzNjQ1.olRPpoZvIcqkn2Oyigqjm3QVCxOKYVv6KO3eFmSGrXEg.hI6AEufHwEkYucJvILBxce4xK-ZLgc-XfLcj5KF0Jl8g.PNG.ks06891%2Fimage.png&type=sc960_832)


## ps 명령어

`ps` 명령어는 현재 실행 중인 프로세스의 스냅샷을 제공하는 유틸리티입니다.

### ps 명령어 옵션

-e : 실행중인 모든 프로세스의 정보를 출력한다.

-f : 프로세스에 대한 자세한 정보를 출력한다.

-u[사용자이름] : 특정 사용자에 대한 모든 프로세스의 정보를 출력

-p pid : pid로 지정한 프로세스의 정보를 출력

u : 프로세스 소유자의 이름, cpu사용량, 메모리 사용량 등 상세정보를 출력

a : 터미널에서 실행한 프로세스의 정보를 출력

x : 실행 중인 모든 프로세스의 정보를 출력


![ps 명령어 실행 예시](https://postfiles.pstatic.net/MjAyMzA0MjVfMjYy/MDAxNjgyNDAxMjc3MTg5.ASKz50XPaVyJN4Tkbggd6rWF0GTi8ym3i5fUttwNrlcg.8CXEJriTwkayowJe98UvV76e6DzN5eblpI-Jdr2LO8Yg.PNG.ks06891/image.png?type=w966)



## jobs 명령어

`jobs` 명령어는 쉘에서 백그라운드로 실행 중인 작업의 목록을 보여줍니다.

### jobs 명령어 옵션

-l : 프로세스 그룹 ID를 state 필드 앞에 출력

-n : 프로세스 그룹중에 대표 프로세스 ID를 출력

-p : 각 프로세스 ID에 대해 한 행씩 출력

command : 지정한 명령어를 실행


![jobs 명령어 실행 예시](https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2FMjAyMjA0MTFfMTMx%2FMDAxNjQ5NjYxNDIwNDMw.zWyMG7HEtmWIk2M0ghXpIaz7ixttnpWoS6VhB2x51Ksg.nSq7OTgHjN9nWn6-MxrydsGNY-sBSSMDskgRJGDzxF0g.JPEG.mcoding777%2F9.JPG&type=sc960_832)



## kill 명령어

`kill` 명령어는 실행 중인 프로세스를 종료하는 데 사용됩니다.

## kill 명령어 옵션

-l : 시그널의 종류를 나열한다. 시그널의 종류는 시그널 번호순서대로 나열한다.

## `[signal_number와 이름]`

1 SIGHUP(HUP) : hang up의 약자로 프로세스를 재시작시키는 시그널이다.

2 SIGINT(INT) : 인터럽트. 실행을 중지시킨다. [CTRL] + [C] 를 눌렀을 때 보내지는 시그널
이다.

3 QUIT : 키보드 종료. 

9 SIGKILL(KILL) : 무조건 종료, 즉 강제 종료시키는 시그널이다.

15 SIGTERM(TERM) : Terminate의 약자로 가능한 정상 종료시키는 시그널로 kill 명령의 기본
시그널이다.

18 CONT : Continue. STOP등에 의해 정지된 프로세스를 다시 실행시킨다.

19 STOP : 무조건적, 즉각적 정지

20 TSTP : 실행 정지후 다시 실행을 계속하기 위하여 대기시키는 시그널이다. [CTRL] +[Z] 를 
눌렀을 때 보내지는 시그널이다.


![kill 명령어 실행 예시](https://postfiles.pstatic.net/MjAyMjA0MTFfMTMx/MDAxNjQ5NjYxNDIwNDMw.zWyMG7HEtmWIk2M0ghXpIaz7ixttnpWoS6VhB2x51Ksg.nSq7OTgHjN9nWn6-MxrydsGNY-sBSSMDskgRJGDzxF0g.JPEG.mcoding777/SE-d9c0a84d-1e3b-4a51-99e9-bfec65cc472a.jpg?type=w966)

# 요약

| 명령어 | 설명 | 사용법 |
|--------|------|--------|
| top | 시스템의 실시간 프로세스 모니터링 도구로, CPU, 메모리 사용량, 프로세스 정보 등을 보여줍니다. | `top [옵션]` |
| ps | 현재 실행 중인 프로세스 정보를 보여주는 명령어입니다. | `ps [옵션]` |
| jobs | 현재 쉘에서 실행 중인 백그라운드 작업 목록을 보여줍니다. | `jobs [옵션] [작업번호]` |
| kill | 실행 중인 프로세스를 종료하는 명령어입니다. | `kill [옵션] [프로세스ID]` | 

-나*-나*-나* 
