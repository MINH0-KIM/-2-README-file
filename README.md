# 과제2-조사내용 README파일로  정리하기
- 리눅스 명령어와 vim 에디터에서 매크로 관련하여 조사
1. [리눅스 명령어 : top, ps, jobs, kill 명령어 조사하기](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#1-%EB%A6%AC%EB%88%85%EC%8A%A4-%EB%AA%85%EB%A0%B9%EC%96%B4--top-ps-jobs-kill-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%A1%B0%EC%82%AC%ED%95%98%EA%B8%B0)
   - [top](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#top)
      - [사용법 및 옵션](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#%EC%82%AC%EC%9A%A9%EB%B2%95-%EB%B0%8F-%EC%98%B5%EC%85%98)
      - [설명](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#%EC%84%A4%EB%AA%85)
      - [top 단축키 명령어](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#top-%EB%8B%A8%EC%B6%95%ED%82%A4-%EB%AA%85%EB%A0%B9%EC%96%B4)
      - [top 보기 수정 단축키](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#top-%EB%B3%B4%EA%B8%B0-%EC%88%98%EC%A0%95-%EB%8B%A8%EC%B6%95%ED%82%A4)
      - [top 정렬 단축키](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#top-%EC%A0%95%EB%A0%AC-%EB%8B%A8%EC%B6%95%ED%82%A4)
      - [top 항목에 대한 설명](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#top-%ED%95%AD%EB%AA%A9%EC%97%90-%EB%8C%80%ED%95%9C-%EC%84%A4%EB%AA%85)
   - [ps](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#ps)
     - [사용법 및 옵션](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#%EC%82%AC%EC%9A%A9%EB%B2%95-%EB%B0%8F-%EC%98%B5%EC%85%98-1)
     - [주요 명령어](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#%EC%A3%BC%EC%9A%94-%EB%AA%85%EB%A0%B9%EC%96%B4)
     - [설명](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#%EC%84%A4%EB%AA%85-1)
     - [자주 사용하는 ps 옵션의 조합](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#%EC%9E%90%EC%A3%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-ps-%EC%98%B5%EC%85%98%EC%9D%98-%EC%A1%B0%ED%95%A9)
   - [jobs](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#jobs)
   - [kill](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#kill)
2. [vim 에디터에서 매크로 사용방법에 대하여 조사하기 (q , @)](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#2-vim-%EC%97%90%EB%94%94%ED%84%B0%EC%97%90%EC%84%9C-%EB%A7%A4%ED%81%AC%EB%A1%9C-%EC%82%AC%EC%9A%A9%EB%B0%A9%EB%B2%95%EC%97%90-%EB%8C%80%ED%95%98%EC%97%AC-%EC%A1%B0%EC%82%AC%ED%95%98%EA%B8%B0-q--)
   - [매크로](https://github.com/MINH0-KIM/-2-README/edit/main/README.md#%EB%A7%A4%ED%81%AC%EB%A1%9C)

## 1. 리눅스 명령어 : top, ps, jobs, kill 명령어 조사하기

### top
>요약 시스템 프로세스/메모리 사용 현황을 실시간으로 출력한다.
#### 사용법 및 옵션

    top [옵션]
    
- **-b** : 배치모드로 정보를 출력한다. 실시간 상화 대화형모드로 정보를 화면에 일렬로 출력한다.
- **-d delay** : 지정한 시간(**delay** 초)의 간격으로 정보를 업데이트하여 출력한다.
- **-i idle** : 토글값이 off일 때, **idle** 프로세스나 좀비 프로세스 정보를 출력하지 않는다.
- **-n num** : 지정한 시간(**num**)만큼 업데이트 정보를 출력한다.
- **-p pid** : 지정한 프로세스 ID(**pid**)의 정보만을 출력한다.
- **-q** : 시간의 간격 없이 계속하여 업데이트 정보를 출력한다.
- **-s** : 몇 개의 대화식 명령을 비활성화한다(시큐어 모드).
- **-S** : 누적된 정보를 출력한다(cumulative 모드).

#### 설명
>top 명령어는 시스템의 프로세스/메모리 사용 상태를 5초의 간격으로 업데이트하여 출력한다.\
>화면에 출력되는 기본값은 현재시간, 시스템 업데이트(1) 시간, 시스템에 로그인한 사용자 수,\
>지난 1분, 지난 5분, 지난 15분간의 시스템 평균 부하를 출력한다.\
>이 목록 아래에 프로세스 정보, CPU 상태, 메모리와 스왑 상태를 출력한다.\
>top 명령어를 실행한 후 초기 화면에서 **h** 키를 입력하면 사용할 수 있는 단축키 목록을 확인할 수 있다.

#### top 단축키 명령어

|명령어|설명|
|:----:|---|
|**space**|정보를 업데이트한다.|
|**^L**|스크린을 다시 초기화한다.|
|**F or f**|필드를 추가나 제거한다. 아래 ‘top 항목에 대한 설명’을 참조한다.</br>확인하고자 하는 항목의 알파벳을 누를 때마다 선택/취소가 반복된다.|
|**O or o**|출력하는 필드의 정렬 순서를 변경한다. 아래 ‘top 항목에 대한 설명’을 참조하자.</br>대문자로 선택한 항목을 누르면 왼쪽으로 이동하고 소문자를 누르면 오른쪽으로 이동한다.|
|**h or ?**|사용 가능한 명령어를 출력한다.|
|**k**|프로세스를 종료시킨다.|
|**n or #**|출력할 프로세스의 수를 지정한다.|
|**s**|출력할 정보의 업데이트 시간을 지정한다.|
|**W**|~/.toprc에 설정된 내용을 저장한다.|
|**q**|top을 종료한다.|

#### top 보기 수정 단축키
>출력되는 메인 정보 창 중에 상단의 정보를 수정한다.

|명령어|설명|
|:----:|---|
**S**|cumulative 모드(실시간 정보를 누적 데이터로 보여 줌)를 선택/해제한다.
**i**|dle 프로세스 정보를 출력한다/해제한다.
**I**|rix나 솔라리스 정보를 출력한다/해제한다.
**c**|령행에서 실행한 명령어 자체로 출력한다/해제한다.
**l**|로드 평균 정보를 출력한다/해제한다.
**m**|메모리 정보를 출력한다/해제한다.
**t**|요약된 정보만을 출력한다/해제한다.

#### top 정렬 단축키
>메인 창에서 실행하는 명령으로 현재 정보를 사용자의 요구대로 정렬한다.

|명령어|설명|
|:----:|---|
**r**|프로세스의 우선순위를 변경한다.
**N**|pid 정보를 기준으로 정렬한다.
**A**|age 정보를 기준으로 정렬한다.
**P**|CPU 사용량을 기준으로 정렬한다.
**M**|적재된 메모리 사용량을 기준으로 정렬한다
**T**|시간/누적시간을 기준으로 정렬한다.
**u**|지정한 사용자의 정보만을 출력한다.

#### top 항목에 대한 설명
>필드의 구성을 변경할 때 출력되는 내용을 정리하였다.

|부호|기호|명칭|설명|
|:-:|:--:|----|----|
\*(2)|**A**|PID|프로세스 ID
||**B**|PPID|부모 프로세스 ID
||**C**|UID|사용자 ID(User ID)
\*|**D**|USER|사용자 이름
\*|**E**|%CPU|CPU 사용량
\*|**F**|%MEM|메모리 사용량
||**G**|TTY|사용중인 tty를 출력한다.
\*|**H**|PRI|우선순위
\*|**I**|NI|nice 우선순위 값
||**J**|PAGEIN|페이지 오류 수
||**K**|TSIZE|코드 크기(KB)
||**L**|DSIZE|데이터 + 스택 크기(KB)
\*|**M**|SIZE|가상 이미지 크기(KB)
||**N**|TRS|현재 문자 크기(KB)
||**O**|SWAP|스왑 크기(KB)
\*|**P**|SHARE|분할된 페이지(KB)
||**Q**|A|접근한 페이지 수(KB)
||**R**|WP|쓰기 보호된 페이지 수(KB)
||**S**|D|쓰레기 페이지
\*|**T**|RSS|메모리에 상주하고 있는 현재 페이지의 크기
||**U**|WCHAN|유휴 상태로 있는 함수
\*|**V**|STAT|프로세스 상태
\*|**W**|TIME|CPU 시간
\*|**X**|COMMAND|명령어
||**Y**|LC|마지막으로 사용한 CPU
||**Z**|FLAGS|테스크 플래그
>\*는 현재 사용하고 있다는 뜻이다.

---
### ps
>프로세스의 현재 상태를 출력한다.
#### 사용법 및 옵션

    ps [옵션]

##### 주요 명령어
- **-e** : 커널 프로세스를 제외한 모든 프로세스를 출력한다.\
![e](https://user-images.githubusercontent.com/106523894/171360633-07e805d9-5e70-4ca9-9a6e-323f4b13833d.png)
- **-f** : UID, PID, PPID, C, STIME, TTY, TIME, CMD 등의 필드를 CMD 필드의 전체 명령어 형태로 출력한다.\
![f](https://user-images.githubusercontent.com/106523894/171361490-2a3cb169-5c00-4663-86a8-938cc9626a3e.png)
- **-u [사용자]** : 특정 **사용자**의 프로세스 정보를 출력, **사용자**를 지정하지 않는다면 현재 **사용자** 기준으로 출력\
![u](https://user-images.githubusercontent.com/106523894/171363157-3afc0c3a-7774-435c-9dcd-7033c987dfa0.png)
>ps 명령어는 보통 아래와 같이 grep와 연동해서 사용한다.\
>![그랩](https://user-images.githubusercontent.com/106523894/171359664-78214d2a-d0af-4a18-a57d-1f775700f0ee.png)

##### 설명
>ps 명령어는 프로세스의 현재 상태를 출력한다.
>>**ps와 top의 차이점**
>>- ps는 ps한 시점에 proc에서 검색한 cpu 사용량을 출력한다.
>>- top은 proc에서 일정 주기로 합산해 cpu 사용율을 출력한다
###### 자주 사용하는 ps 옵션의 조합
>표준 문장으로 시스템의 모든 프로세스를 출력한다.
>```
>$ ps -e
>$ ps -ef
>$ ps -eF
>$ ps -ely
>```

>BSD 문장으로 시스템의 모든 프로세스를 출력한다.
>```
>$ ps ax
>$ ps aux
>```

>프로세스 트리를 출력할 수 있다.
>```
>$ ps -ejH
>$ ps axjf
>```

>스레드 정보를 출력한다.
>```
>$ ps -eLf
>$ ps axms
>```

>아래 옵션은 보안 정보를 확인할 수 있다.
>```
>$ ps -eo euser, ruser, suser, fuser, f, comm., lable
>$ ps axZ
>```
---
### jobs
>현재 세션의 작업 상태를 출력한다.
#### 사용법 및 옵션
```
jobs [옵션] [job ID]
jobs -x command [args]
```
- **-l** : 프로세스 그룹 ID를 state 필드 앞에 출력한다.
- **-n** : 프로세스 그룹 중에 대표 프로세스 ID를 출력한다.
- **-p** : 각 프로세스 ID에 대해 한 행씩 출력한다.
- **command** : 지정한 명령어를 실행한다.

#### 설명
>jobs는 작업이 중지된 상태, 백그라운드로 진행 중인 작업 상태, 변경되었지만 보고되지 않은 상태 등을 표시한다.

현재 환경의 작업 상태를 아래와 같이 확인할 수 있다.\
![ka38_149_i2](https://user-images.githubusercontent.com/106523894/171385593-0c8e6c8f-04ee-42b0-876f-4cf9fb261388.jpg)

-l 옵션은 state 필드 앞에 프로세스 ID를 출력한다.\
![ka38_149_i3](https://user-images.githubusercontent.com/106523894/171385661-d8a9e241-a069-4e9e-8671-8654b8dd1df4.jpg)

jobs 명령어로 확인할 수 있는 세션의 상태값은 다음과 같다.
|상태|설명|
|:--:|----|
Running|작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임을 뜻한다.
Done|작업이 완료되어 0을 반환하고 종료했음을 뜻한다.
Done (code)|작업이 정상적으로 완료했으며, 0이 아닌 코드를 반환했음을 뜻한다.
Stopped|작업이 일시 중단됨을 뜻한다.
Stopped (SIGTSTP)|SIGTSTP 신호가 작업을 일시 중단했음을 뜻한다.
Stopped (SIGSTOP)|SIGSTOP 신호가 일시 중단했음을 뜻한다.
Stopped (SIGTTIN)|SIGTTIN 신호가 작업을 일시 중단했음을 뜻한다.
Stopped (SIGTTOU)|SIGTTOU 신호가 작업을 일시 중단했음을 뜻한다.


>다음과 같이 하면 v로 시작하는 모든 프로세스 ID를 확인할 수 있다.\
>![ka38_149_i4](https://user-images.githubusercontent.com/106523894/171386266-a1cb248f-ea15-4074-b67b-f34e3f4bdbfd.jpg)


---
### kill
>프로세스를 종료한다.
#### 사용법 및 옵션
```
    kill [-s시그널][-a]pid...
    kill-l [시그널]
```
- **pid ···** : 종료시킬 프로세스 ID나 프로세스 이름을 지정한다.
- **-s** : 전달할 시그널의 종류를 지정한다. 여기에는 시그널 이름이나 번호를 써준다.
- **-l** : 시그널로 사용할 수 있는 시그널 이름들을 보여준다. 이것은 /usr/include/linux/signal.h 파일에서도 알 수 있다.
- **-1,** : -HUP 프로세스를 재활성화한다.
- **-9** : 프로세스를 강제로 종료시킨다.

#### 설명
>kill 명령어는 프로세스에 종료 시그널을 보낸다. 시스템에 얘기치 않은 문제가 생긴 프로세스를 종료시킬 수 있다.
>만일 kill 명령으로 종료되지 않는 프로세스는 -9 옵션을 사용해서 강제로 종료하면 된다.

>아래와 같이 ps 명령어로 sshd 프로세스를 확인할 수 있다.
>>![kii](https://user-images.githubusercontent.com/106523894/171415223-c6b2922f-a44d-4798-9b5a-bd7587479a1e.png)\
>>현재 sshd 프로세스는 root 사용자 권한으로 동작하고 있으며 PID는 2518와 12095이다. 

참고로 ps aux 명령에서 볼 수 있는 프로세스 정보에 대한 각각의 필드 내용은 다음과 같다.

|내용|명칭|설명|
|:--:|:--:|---------------|
root|USER|프로세스의 사용자
2518|PID|프로세스 ID
0.0|%CPU|마지막 1분 동안 프로세스가 사용한 CPU 점유율
0.1|%MEM|마지막 1분 동안 프로세스가 사용한 메모리의 점유율
7084|VSZ|가상메모리에 있는 프로세스의 KB 단위 크기
1076|RSS|프로세스의 실제 메모리의 크기로 KB 단위
?|TTY|연결되어 있는 터미널
Ss|STAT|실행되고 있는 프로세스 상태
Jun07|START|프로세스가 시작된 날짜
0:00|TIME|프로세스가 소비한 총 시간
/usr/sbin/sshd|COMMAND|사용자가 실행한 명령 이름

ps 명령으로 확인한 PID를 이용하면 원하는 프로세스를 종료시킬 수 있다.\
![ka38_154_i3](https://user-images.githubusercontent.com/106523894/171413388-4fe4f0a0-d607-4fd6-a753-bd63b078c11b.jpg)
>만일 kill 명령으로 종료되지 않으면 **-9** 옵션으로 강제 종료할 수 있다.
>![ka38_154_i4](https://user-images.githubusercontent.com/106523894/171413611-90aefc6f-7b9f-4967-a268-5b1a66c90ecd.jpg)
>>PID 1은 init을 의미하기 때문에 만일 **kill -9 1** 명령을 수행한다면 시스템이 다운된다.

**kill -HUP pid** 명령을 이용하면 프로세스를 종료 후 다시 재실행한다.
![ka38_154_i5](https://user-images.githubusercontent.com/106523894/171413944-9eb77873-d572-4a9d-b297-6e5e97a1e1f4.jpg)

#### 시그널
>시그널(Signal)은 유닉스 시스템에서 프로세스간 통신을 하는 가장 오래된 방법으로, \
>프로세스에 비동기적인 이벤트를 전달하는데 사용한다.\
>이와 같은 시그널은 키보드 인터럽트나 에러 상황이 일어났을 때 발생한다.\
>또한 셸이 자식 프로세스에 작업 명령을 보낼 때에도 사용한다.\
>이러한 시그널의 목록은 **kill -l** 명령으로 확인할 수 있다.
>>![ka38_154_i6](https://user-images.githubusercontent.com/106523894/171415818-94bc1518-93d4-4aa5-adee-93c37cd48575.jpg)\
>>
>>프로세스는 대부분의 시그널을 무시할 수 있지만, **9번(SIGKILL)과 19번(SIGSTOP)** 시그널은 무시할 수 없다.\
>>앞서 kill을 설명할 때 뒤따라 붙던 숫자가 바로 이 시그널 번호이다.\
>>프로세스가 시그널을 받으면 이 시그널을 블록할 수도 있으며 직접적으로 처리하거나 혹은 커널에 제어권을 넘길 수도 있다.\
>>커널에 넘어가면 이 시그널이 동작대로 움직인다.

## 2. vim 에디터에서 매크로 사용방법에 대하여 조사하기 (q , @)

### 매크로
>녹화된 키로그를 반복 실행한다.
#### 사용법 및 단축키
|기능|일반모드|EX|
|--|-----|----|
녹화|**q+(매크로KEY)**|qa
녹화종료|**q**|q
재생|**@+(매크로KEY)**|@a
마지막매크로실행|**@@**|@@
횟수실행|**(횟수)@(매크로KEY)**|10@a
#### EX
1. 일반모드에서 **q+a** 입력\
![시작](https://user-images.githubusercontent.com/106523894/171425549-6274624d-9e3c-4f27-87bd-f5686dd9268f.png)
2. vim 상태바에 **recording @a** 표시\
![매크로](https://user-images.githubusercontent.com/106523894/171426189-eb109bb2-44ad-4508-8949-d6e3a1e2b48f.png)
3. 매크로 기록\
![매크로 작성](https://user-images.githubusercontent.com/106523894/171426955-7dc1aa69-276d-4985-bdc9-62723ddfd285.png)
4. **q**를 입력해 녹화 종료\
![매크로 끝](https://user-images.githubusercontent.com/106523894/171427244-50ef041e-a9d0-40e1-8198-53c5910584fe.png)
5. **@a**로 매크로 실행\
![매크로 사용](https://user-images.githubusercontent.com/106523894/171427668-2d1d59e3-cfb0-4fca-a9ea-b02dd9081714.png)
