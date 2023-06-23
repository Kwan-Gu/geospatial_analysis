# 공간분석 스터디

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

## 배포 과정
### 1. 빌드
```commandline
jb build --all .\automating_gis_processes\
```
### 2. 배포
```commandline
ghp-import -n -p -f .\automating_gis_processes\_build\html\
```
