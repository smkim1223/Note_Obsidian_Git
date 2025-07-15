# 마크다운1
## 마크다운2
### 마크다운3
#### 마크다운4
- '-' bullet
	- by tap
	- [ ] '[ ]' can make a todo list
- [ ] 'shift tap'

1. '1.' making a new number
2. likely Notion

double '[[]]' making a link for a note

How about template and table

# LaTeX 수식 문법 정리 (기초부터 자주 쓰는 예시까지)
LaTeX는 수학 및 과학 문서를 위한 고급 조판 언어입니다. 옵시디언(Obsidian), 마크다운, 논문 등 다양한 곳에서 사용할 수 있으며, `$...$` 또는 `$$...$$` 안에 입력하면 수식이 렌더링됩니다.
## ✅ 기본 구조

- `$수식$` : **인라인 수식**
- `$$수식$$` : **블록 수식** (중앙 정렬)

## ✅ 기초 문법 정리

| 목적            | 문법 예시                         | 출력 결과                         |
|-----------------|-----------------------------------|-----------------------------------|
| 덧셈, 뺄셈, 곱셈, 나눗셈 | `a + b`, `a - b`, `a \times b`, `a \div b` | a + b, a − b, a × b, a ÷ b        |
| 분수           | `\frac{a}{b}`                     | $$\frac{a}{b}$$                   |
| 제곱, 지수     | `x^2`, `e^{i\pi} + 1 = 0`        | $$x^2$$, $$e^{i\pi} + 1 = 0$$     |
| 밑             | `x_1`, `a_{ij}`                  | $$x_1$$, $$a_{ij}$$               |
| 괄호 확대      | `\left( \frac{a}{b} \right)`     | $$\left( \frac{a}{b} \right)$$    |
| 루트           | `\sqrt{x}`, `\sqrt{x}`         | $$\sqrt{x}$$, $$\sqrt{x}$$     |
| 적분           | `\int_0^1 x^2 dx`                 | $$\int_0^1 x^2 dx$$               |
| 합, 곱         | `\sum_{i=1}^{n} i`, `\prod_{i=1}^{n} i` | $$\sum_{i=1}^{n} i$$, $$\prod_{i=1}^{n} i$$ |
| 행렬           | `\begin{bmatrix} a & b \\ c & d \end{bmatrix}` | $$\begin{bmatrix} a & b \\ c & d \end{bmatrix}$$ |

## ✅ 기호 및 특수 문자

| 의미       | LaTeX 문법       | 출력 결과   |
|------------|------------------|-------------|
| 알파벳(그리스) | `\alpha`, `\beta`, `\theta` 등 | $$\alpha, \beta, \theta$$ |
| 무한대     | `\infty`         | $$\infty$$   |
| 근사값     | `\approx`        | $$\approx$$  |
| 같음/부등호 | `=`, `\ne`, `\le`, `\ge` | $$=, \ne, \le, \ge$$ |
| 소속       | `\in`, `\notin`  | $$\in, \notin$$ |
| 부분집합   | `\subset`, `\subseteq` | $$\subset$$, $$\subseteq$$ |

## ✅ 정렬된 여러 줄 수식

여러 줄로 정렬하려면 `align` 환경을 사용합니다:

```latex
\begin{align}
a + b &= c \\
x^2 + y^2 &= z^2
\end{align}
```

👉 옵시디언에서는 `$$ ... $$` 블록 안에 위 내용을 넣으면 정렬된 수식이 표시됩니다.

## ✅ 예제

```latex
$$
E = mc^2
$$
```
출력:  
$$E = mc^2$$

## ✅ 옵시디언에서 사용 팁

- **수식 입력 시 띄어쓰기나 줄바꿈은 무시**되므로, LaTeX 문법만 정확하면 한 줄에 길게 작성해도 OK.
- 복잡한 수식은 `$$`로 묶는 **블록 수식** 작업이 더 깔끔하게 보입니다.
- 옵시디언에서 실시간 렌더링이 잘 안 보인다면 미리보기 모드로 전환해 확인하세요.

필요하다면 고급 수식(예: 미분방정식, 수학기호 TeX 패키지 등)도 도와드릴 수 있어요! 원하시는 수식을 알려주시면 직접 LaTeX로 작성해 드릴게요 😊

Sources


# 옵시디언 주요 기능
## 옵시디언(Obsidian) 마크다운 및 링크 등 주요 기능 사용법

### 1. 기본 마크다운(Markdown) 문법

Obsidian은 표준 마크다운 문법을 지원하며, 주요 서식은 다음과 같습니다:

| 기능             | 문법 예시                                            | 결과 예시           |
|------------------|------------------------------------------------------|---------------------|
| 제목(Headings)   | `# 제목1`<br>`## 제목2`<br>`### 제목3`               | 제목1, 제목2, 제목3 |
| 굵게(Bold)       | `**굵게**`                                            | **굵게**            |
| 기울임(Italic)   | `*기울임*`                                            | *기울임*            |
| 취소선           | `~~취소선~~`                                          | ~~취소선~~          |
| 하이라이트       | `==강조==`                                            | ==강조==            |
| 인용문           | `> 인용문`                                            | > 인용문            |
| 코드(인라인)     | `` `코드` ``                                          | `코드`              |
| 코드 블록        | <pre>```python<br>print("Hello")<br>```
| 목록(번호/순서)  | `1. 첫 번째`<br>`- 두 번째`                           | 1. 첫 번째<br>- 두 번째 |
| 체크박스(할 일)  | `- [ ] 할 일`<br>`- [x] 완료`                         | - [ ] 할 일<br>- [x] 완료 |
| 구분선           | `---`                                                 | ―――                |
| 표(Table)        | <pre>\|A\|B\|<br>\|---\|---\|<br>\|1\|2\|</pre>      | 표                  |
| 수식(Math)       | `$x^2 + y^2 = z^2$`                                   | $$x^2 + y^2 = z^2$$ |

더 많은 문법은 Obsidian 공식 문서에서 확인할 수 있습니다[1][2][3].

### 2. 링크 기능

#### 내부 링크(노트 간 연결)

- **기본 위키링크:**  
  `[[노트이름]]`  
  → 해당 노트로 바로 이동

- **표시 텍스트 변경:**  
  `[[노트이름|표시할 텍스트]]`  
  → 표시할 텍스트로 링크 표시

- **헤더(제목)로 링크:**  
  `[[노트이름#헤더이름]]`  
  → 특정 헤더(섹션)로 바로 이동

- **블록(문단) 링크:**  
  `[[노트이름#^블록ID]]`  
  → 특정 블록(문단)으로 이동

#### 외부 링크(웹 등)

- `[표시텍스트](https://example.com)`  
  → 웹사이트 등 외부로 연결

#### 파일 및 이미지 첨부

- `![[이미지.png]]`  
  → 노트 내 이미지 삽입

- 외부 이미지:  
  ``  
  → 외부 이미지 삽입

### 3. 기타 주요 기능

- **백링크(Backlink):**  
  어떤 노트가 현재 노트를 참조하고 있는지 자동으로 확인 가능 (오른쪽 사이드바 Backlinks 탭).

- **그래프 뷰:**  
  노트 간 연결 관계를 시각적으로 확인 가능.

- **태그:**  
  `#태그명` 입력 시 태그로 자동 인식, 태그별로 노트 정리 가능.

- **할 일(Task) 관리:**  
  체크박스 문법(`- [ ]`, `- [x]`)으로 할 일 관리.

- **라이브 프리뷰/소스 모드:**  
  마크다운 문법을 실시간으로 렌더링하거나, 원본 마크다운을 직접 편집 가능[4].

### 4. 활용 팁

- `[[` 입력 시 자동 완성 기능으로 기존 노트, 헤더, 블록 등 빠르게 검색 및 링크 가능.
- 링크가 걸린 노트가 아직 없으면, 클릭 시 새 노트로 바로 생성.
- 커맨드 팔레트(Cmd/Ctrl+P)에서 다양한 명령어 및 플러그인 기능 활용 가능.
- 마크다운 표, 수식, 코드 하이라이트 등 고급 문법도 지원[2][3].

### 5. 요약 표: 자주 쓰는 마크다운 및 링크 문법

| 기능            | 입력 예시                        | 설명                         |
|-----------------|----------------------------------|------------------------------|
| 내부 링크       | `[[노트이름]]`                   | 다른 노트로 이동             |
| 내부 링크(별칭) | `[[노트이름|표시이름]]`          | 표시이름으로 링크 표시       |
| 헤더로 링크     | `[[노트이름#헤더]]`              | 특정 헤더(섹션)로 이동       |
| 외부 링크       | `[구글](https://google.com)`     | 외부 웹사이트로 연결         |
| 이미지 첨부     | `![[이미지.png]]`                | 노트 내 이미지 삽입          |
| 체크박스        | `- [ ] 할 일`                    | 할 일 목록                   |
| 표             | `\|A\|B\|` 등 마크다운 표 문법   | 표 생성                      |
| 수식           | `$수식$`                          | 수식 입력                    |

**참고:**  
더 자세한 문법과 활용법은 Obsidian 공식 도움말 및 마크다운 가이드에서 확인할 수 있습니다[1][2][3][5].

[1]
[2]
[3]
[5]

Sources
[1] Basic formatting syntax - Obsidian Help https://help.obsidian.md/syntax
[2] Obsidian Markdown Reference https://www.markdownguide.org/tools/obsidian/
[3] Markdown Syntax - Obsidian Hub https://publish.obsidian.md/hub/04+-+Guides,+Workflows,+&+Courses/Guides/Markdown+Syntax
[4] Views and editing mode - Obsidian Help https://help.obsidian.md/edit-and-read
[5] Link notes - Obsidian Help https://help.obsidian.md/Getting+started/Link+notes
[6] Obsidian markdown : r/ObsidianMD - Reddit https://www.reddit.com/r/ObsidianMD/comments/1aeipqs/obsidian_markdown/
[7] advanced_linking - Obsidian Publish https://publish.obsidian.md/active-inference/docs/tools/advanced_linking
[8] Is it possible to insert hyperlinks into Obsidian? - Reddit https://www.reddit.com/r/ObsidianMD/comments/lt6k23/is_it_possible_to_insert_hyperlinks_into_obsidian/
[9] Obsidian Tutorial - Basics of Formatting (in Markdown) - YouTube https://www.youtube.com/watch?v=9ft9G6JUfO0
[10] Creating and Working with Links in Obsidian - It's FOSS https://itsfoss.com/obsidian-create-links/
[11] Make "insert markdown link" more functional - Obsidian Forum https://forum.obsidian.md/t/make-insert-markdown-link-more-functional/49767
[12] Use Obsidian (BEST Markdown editor) for note taking and tech docs! https://www.youtube.com/watch?v=cBzc5r-FNW0
[13] Links - Fork My Brain https://notes.nicolevanderhoeven.com/obsidian-playbook/Using+Obsidian/03+Linking+and+organizing/Links
[14] Markdown Formatting Guide for Obsidian - GitHub Gist https://gist.github.com/saharshbhansali/5da604f1731c7d5ea07b2bd91552d48c
[15] How to Create Links in Obsidian https://www.alphr.com/obsidian-how-to-create-links/
[16] Links and references with Markdown syntax (local resources) - Help https://forum.obsidian.md/t/links-and-references-with-markdown-syntax-local-resources/66017
[17] Obsidian Configuration to any Markdown Documentation - Help https://forum.obsidian.md/t/obsidian-configuration-to-any-markdown-documentation/92844
[18] Internal links - Obsidian Help https://help.obsidian.md/links
[19] Markdown for Obsidian - File Linking and Embedding - YouTube https://www.youtube.com/watch?v=mk3YCfaZHq8
[20] Every USEFUL Markdown Syntax That I Use in Obsidian https://www.youtube.com/watch?v=d8fXEhWy_rY

# 옵시디언(Obsidian)에서 테이블과 수식 넣는 방법

옵시디언은 마크다운 기반 노트 앱으로, **테이블 작성과 수식 입력**을 모두 지원합니다. 아래에 각각의 방법을 자세히 설명합니다.

## 1. 옵시디언에서 테이블 작성하는 방법

옵시디언은 기본적으로 마크다운 표기법을 사용해 테이블을 작성합니다.

### 기본 마크다운 테이블 문법

```markdown
| 헤더1 | 헤더2 | 헤더3 |
|-------|-------|-------|
| 내용1 | 내용2 | 내용3 |
| 내용4 | 내용5 | 내용6 |
```


| name | age | Job
-

- `|` 기호로 각 셀을 구분합니다.
- 두 번째 줄은 `-`와 `|`로 헤더와 본문을 구분하며, `-` 개수는 자유롭습니다.
- 셀 간 간격은 가독성을 위해 띄워 쓰는 것이 좋습니다.

### 예시

| 이름   | 나이 | 직업    |
|--------|-------|---------|
| 홍길동 | 30    | 개발자  |
| 김철수 | 25    | 디자이너 |

### 추가 팁

- 옵시디언에서는 테이블을 작성하면 **에디터 모드에서 자동으로 표 형태로 변환**되어 편집이 편리합니다.
- 셀 내에서 줄바꿈하려면 `<br>` 태그를 사용할 수 있습니다.
- 복잡한 표 편집을 위해 커뮤니티 플러그인 중 **"Advanced Tables"**를 설치하면 편리한 기능(자동 정렬, 셀 이동 등)을 사용할 수 있습니다.

## 2. 옵시디언에서 수식 넣는 방법

옵시디언은 LaTeX 수식 문법을 지원하여, 수식을 깔끔하게 표현할 수 있습니다.

### 인라인 수식

- `$...$` 사이에 LaTeX 수식을 입력합니다.
- 예: `이것은 인라인 수식입니다: $E=mc^2$`

$E=mc^2$


### 블록 수식

- `$$` 사이에 수식을 입력하면 별도의 블록으로 수식이 중앙 정렬되어 표시됩니다.
- 예:
  ```markdown
  $$
  \int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
  $$
  ```

### 수식 작성 팁

- LaTeX 문법을 그대로 사용하므로, 복잡한 수식도 표현 가능
- 수식 렌더링은 MathJax 라이브러리를 사용하여 실시간으로 보여줍니다.
- 수식 앞뒤에 공백을 두면 가독성이 좋아집니다.

## 3. 요약

| 기능       | 작성법 예시                                | 설명                          |
|------------|------------------------------------------|-------------------------------|
| 테이블     | `| 헤더1 | 헤더2 |`<br>`|-------|-------|`<br>`| 내용1 | 내용2 |` | 마크다운 표준 문법 사용           |
| 인라인 수식 | `$E=mc^2$`                              | 문장 중간에 수식 삽입          |
| 블록 수식   | `$$ \int_0^\infty e^{-x^2} dx $$`      | 별도의 블록으로 수식 중앙 정렬 |

필요에 따라 커뮤니티 플러그인을 활용하면 테이블 편집이나 수식 입력이 더 편리해집니다. 추가 질문이 있으면 언제든 문의해 주세요!

Sources


