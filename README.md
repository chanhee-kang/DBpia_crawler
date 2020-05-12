## DBpia 디비피아 크롤러
국내 논문 서지정보 사이트 DBpia내의 논문제목, 저자, 퍼블리셔, 저널명, 볼륨, 날짜, 초록의 내용을 가져올수 있는 프로그램 입니다

### 설치
DBpia 디비피아 크롤러는 파이썬3를 통해 작성되었으며 BeautifulSoup과 셀레늄 패키지를 활용하였습니다.<br><br>
먼저 해당 프로그램을 git clone을 통해 다운로드 해줍니다.
```
$git clone https://github.com/chanhee-kang/DBpia_crawler.git
```
그후, 해당 프로그램을 사용하기 위해서는 자신의 크롬의 버전과 일치하는 크롬드라이버가 필요합니다.<br><br>
크롬드라이버 다운로드는 다음 링크를 통해 설치가 가능합니다. [https://chromedriver.chromium.org/downloads] <br><br>
또한, 아나콘다(Anaconda)환경에서 제작되어서 아나콘다내 파이썬 내장 패키지외 추가 패키지를 터미널에서 pip 명령어를통해 설치 해주어야 합니다
```
$pip install selenium
$pip install beautifulsoup
```

### 실행
아래 코드에 DBpia 내에서 크롤링할 검색어 설정, 날짜, 다운로드 받으신 크롬드라이버의 경로 설정을 해줍니다.
```
searchQ = "검색어 삽입"
startYear = 크롤링 시작 벙위 설정
endYear = 크롤링 마침 벙위 설정

print("start crawling..")

path = 'chromedriver 경로 지정'
```
코드 밑단 부분에 크롤링 결과가 저장될 경로를 삽입시켜줍니다.
```
fName = "{}_{}_{}.csv".format(searchQ, startYear, endYear)
```
코드를 실행시켜 주시면 Selenium을 통한 크롤링이 진행됩니다.

### 보안점
멀티 쓰레딩 추가

### Contact
If you have any requests, please contact: [https://ck992.github.io/](https://ck992.github.io/).

