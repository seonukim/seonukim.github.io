---
layout: post
title:  "마크다운 문법 정리"
date:   2022-08-02
categories: [Study, etc]
tags: [markdown, md]
---

#### 앞으로 블로그에 글을 적기 위해 마크다운 문법을 정리했다.
참고 블로그:[갓대희의 작은 공간](https://goddaehee.tistory.com/307)

## # 1. 제목(Header)
 \- `#` 뒤에 띄어쓰기를 넣어주는게 권장하는 방법  
 \- `<h1> ~ <h6>`까지 표현 가능
 ```html
 # 제목1
 ## 제목2
 ### 제목3
 #### 제목4
 ##### 제목5
 ###### 제목6
 ```
 <br/>
 
## # 2. 줄바꿈 (Line Breaks)
 \- 띄어쓰기 2번 또는 `<br/>`로 표현 가능
 ```html
 줄바꿈<br/>
 줄바꿈
 ```
 <br/>
 
## # 3. 수평선 (Horizontal Rule)
 \- 다음 코드는 모두 수평선을 나타낸다. 가시적으로 페이지를 나누는 용도로 많이 사용됨
 ```html
 ---
 ***
 ___
 ******
 ```
 <br/>
 
## # 4. 글자 강조 (Emphasis)
 \- 다음의 표현을 사용하여 글자를 강조할 수 있음
 ```html
 **굵은 글씨**
 *이탤릭*
 _이탤릭_
 ~~취소선~~
 <u>밑줄</u>
 ```
 **굵은 글씨**  
 *이탤릭*  
 _이탤릭_  
 ~~취소선~~  
 <u>밑줄</u>
 <br/>
 
## # 5. 인용문 (BlockQuote)
 \- **">"** 블럭 인용 문자를 사용하면 인용문 표현이 가능
 ```html
 > 인용문장
 >> 중첩된 인용문
 >>> 중첩된 인용문
 ```
 > 인용문장
 >> 중첩된 인용문
 >>> 중첩된 인용문
 <br/>
 
## # 6. 목록 (List)
 1) 순서가 없는 목록 (*, +, - 지원)
 
```html
 - 순서가 필요하지 않은 목록
 	- 순서가 필요하지 않은 목록
		- 순서가 필요하지 않은 목록
 * 순서가 필요하지 않은 목록
	* 순서가 필요하지 않은 목록
		* 순서가 필요하지 않은 목록
 - 순서가 필요하지 않은 목록
    - 순서가 필요하지 않은 목록
		- 순서가 필요하지 않은 목록
 - 순서가 필요하지 않은 목록
    * 순서가 필요하지 않은 목록
		* 순서가 필요하지 않은 목록
```
 
 2) 순서가 있는 목록

```html
 1. 순서가 필요한 목록
 	1. 순서가 필요한 목록
	1. 순서가 필요한 목록
 1. 순서가 필요한 목록
 
 1. 순서가 필요한 목록
 	9. 순서가 필요한 목록
	3. 순서가 필요한 목록
 8. 순서가 필요한 목록
```
 <br/>
 
## # 7. 링크 (Links)
 1) 기본방법<br/>
 ```html
 [Title](link)
 ```
 2) 참조링크<br/>
 ```html
 [link kwd][id]
 ※ [id]: URL "Optional Title
 ```
 <br/>
 
## # 8. 이미지 (Images)
 \- 링크와 문법이 유사함, 앞에 **`!`**만 추가하면 됨<br/>
 1) 기본문법
 ```html
 ![대체텍스트](이미지주소)
 ``` 
 2) 참조 링크
 ```html
 :[대체텍스트][id]
 [id]: 이미지주소 "Optional Title"
 ```
 3) 이미지 노출과 동시에 링크 걸기<br/>
 ```html
 [![대체텍스트](이미지주소)](링크주소)
 ```
 <br/>
 
## # 9. 표 (Table)
 \- **`| (vertical bar)`** 기호를 통해 테이블을 표현 가능. (가장 좌측, 우측은 생략 가능)<br/>
 \- 헤더와 셀을 구분할 때 3개 이상의 `-`(하이픈, 대시)가 필요하다.<br/>
 \- **`: (콜론)`** 기호를 통해 정렬할 수 있다.
 ```html
 | Header | value | Description |
 | --: | :-- | :--: |
 | 정렬 | --: | 우측정렬 |
 | 정렬 | :-- | 좌측정렬 |
 | 정렬 | :--: | 가운데정렬 |
 ```
 
 | Header | value | Description |
 | --: | :-- | :--: |
 | 정렬 | --: | 우측정렬 |
 | 정렬 | :-- | 좌측정렬 |
 | 정렬 | :--: | 가운데정렬 |
 
 <br/>
 
## # 10. 코드 (Code)
 1) 인라인 코드 (Inline Code)<br/>
  \- `-` 백틱( \`: 숫자 1번 키 왼쪽에 위치)으로 강조할 내용을 감싸줌<br/>
  \- `해당 코드`는 강조할 부분
  
 2) 블럭 코드 (Block Code)<br/>
 \- ```html, css, javascript, bash, plaintext 등등<br/>
 \- 코드의 종류를 명시하지 않은 경우
 ```
 <a href="https://seonu-devlog.run.goorm.io" title="Seonu's Devlog">Seonu's Devlog</a>
 ```
 \- html
 ```html
 <a href="https://seonukim.github.io"
 	title="Seonu's Devlog">Seonu's Devlog</a>
 ```
 \- CSS
 ```css
 div {
 	background=color: red;
 }
 ```
 \- javascript
 ```javascript
 const name = "선우";
 console.log(name);
 ```
 \- bash
 ```bash
 $ls -al
 ```
 \- 이외 텍스트 (plaintext)
 ```plaintext
 코드 이외의 텍스트들
 ```
 <br/>
 
## # 11. 원시 HTML (Raw HTML)
 \- 마크다운 환경에서는 표현의 한계가 있음, 이럴 때 순수 HTML 문법을 사용할 수 있음.<br/>
 \- ex) image를 표현할 때 마크다운으로는 width 지정이 불가능하다.
 ```html
 <img width="70" src="" alt="gods"/>
 ```
 ex) 링크를 표현할 때 `target="_blank"` 지정이 불가능하다.<br/>
 ex) 밑줄을 표현할 수 없어 `<u></u>`를 사용하거나 다음과 같이 `style`을 직접 지정해주어야 한다.
 ```html
 <span style="text-decoration: underline;">Seonu's</span>Devlog
 ```