# 공간정보분석 Ⅰ - Automating GIS Processes

&emsp;《Automating GIS Processes》를 **한국어로 번역 및 자료를 현지화**한 웹페이지 입니다.  

## 파일 설명
- Configuration file : _config.yml  
- Table of contents file : _toc.yml  

## _config.yml  
- `title` : 책 제목. 왼쪽 사이드바에 표시  
- `author` : 저자  
- `logo` : 로고 이미지. 사이드바에 표시  
- `execute` : Execution and Cacheing 관리  
  - `execute_notebooks: "force"` : 빌드시 주피터노트북 실행  
- `bibtex_bibfiles` : Citation 관련  

## _toc.yml  
- `format` : `jb-article` 또는 `jb-book`  
- `root` : 시작 페이지  
- `chapters` : (`jb-book`일 때 한정) 단원 파일들  

## 이미지 붙이는 마크다운  
````md
```{figure} ../images/C-3PO_droid.png
---
height: 150px
name: directive-fig
---
Here is my figure caption!
```
````

## 댓글 기능 추가
````md
```{raw} html
<script src="https://utteranc.es/client.js"
        repo="Kwan-Gu/geospatial_analysis"
        issue-term="pathname"
        theme="preferred-color-scheme"
        crossorigin="anonymous"
        async>
</script>
```
````

## 배포 과정
### 1. requirements.txt 업데이트
```commandline
pip freeze > automating_gis_processes/requirements.txt
```
### 2. 빌드
```commandline
jb build --all .\automating_gis_processes\
```
### 3. 배포
```commandline
ghp-import -n -p -f .\automating_gis_processes\_build\html\
```

## 커밋 메세지  
| Type 키워드 | 사용 시점                                     |
| -------- | --------------------------------------------- |
| feat     | 새로운 기능 추가                                 |
| fix      | 버그 수정                                       |
| docs     | 문서 수정                                       |
| style    | 코드 스타일 변경 (코드 포매팅, 세미콜론 누락 등)<br>기능 수정이 없는 경우 |
| design   | 사용자 UI 디자인 변경 (CSS 등)                    |
| test     | 테스트 코드, 리팩토링 테스트 코드 추가               |
| refactor | 코드 리팩토링                                    |
| build    | 빌드 파일 수정                                   |
| ci       | CI 설정 파일 수정                                |
| perf     | 성능 개선                                       |
| chore    | 빌드 업무 수정, 패키지 매니저 수정 (gitignore 수정 등) |
| rename   | 파일 혹은 폴더명을 수정만 한 경우                     |
| remove   | 파일을 삭제만 한 경우                               |
