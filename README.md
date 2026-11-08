# ✈️ Aviation Quiz Game
### Python으로 만드는 나만의 항공·공항 상식 퀴즈 게임

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%2011-blue)
![Git](https://img.shields.io/badge/Git-Version%20Control-orange)
![Data](https://img.shields.io/badge/Data-JSON-green)

---

## 1. 프로젝트 개요

### 프로젝트명
Aviation Quiz Game (항공·공항 상식 퀴즈 게임)

### 프로젝트 소개

본 프로젝트는 Python을 활용하여 항공 및 공항 분야의 기초 지식을 학습할 수 있는 콘솔 기반 퀴즈 게임을 제작하는 것을 목표로 한다.

사용자가 메뉴에서 원하는 기능을 선택하여 퀴즈를 풀거나 새로운 문제를 등록하고, 전체 퀴즈 목록과 최고 점수를 확인할 수 있도록 구현한다.

Python의 변수, 자료형, 조건문, 반복문, 함수 및 객체 지향 프로그래밍을 활용하여 프로그램을 구성한다.

또한 JSON 파일을 이용하여 퀴즈 데이터와 최고 점수를 저장하고, 프로그램을 종료한 후 다시 실행해도 기존 데이터가 유지되도록 구현한다.

Git을 활용하여 기능별 변경 이력을 관리하고, 브랜치 생성 및 병합을 수행한 후 GitHub에 프로젝트를 업로드한다.

### 프로젝트 목표

- Python 기본 문법 이해 및 활용
- 변수와 자료형 활용
- if/elif/else 조건문 구현
- for 및 while 반복문 활용
- 함수와 반환값 활용
- Quiz 및 QuizGame 클래스 구현
- JSON 파일 저장 및 불러오기
- try/except 예외 처리
- Git 커밋 및 브랜치 관리
- GitHub 저장소 업로드 및 협업 방식 이해

---

## 2. 퀴즈 주제 선정 이유

### 주제: 항공·공항 상식

평소 항공기와 공항 운영 분야에 관심이 있어 항공 관련 지식을 Python 프로그램으로 구현하고자 본 주제를 선정하였다.

항공기 종류, 공항 시설, 항공 안전, 항공 직업 등 다양한 내용을 퀴즈로 구성하여 프로그래밍 학습과 항공 분야 지식 습득을 함께 진행하고자 한다.

특히 직접 문제를 추가하고 저장할 수 있는 기능을 구현하여 사용자가 지속적으로 퀴즈 데이터를 확장할 수 있도록 설계한다.

---

## 3. 개발 환경

| 구분 | 개발 환경 |
|---|---|
| OS | Windows 11 |
| Programming Language | Python 3.10 이상 |
| Code Editor | Visual Studio Code |
| Version Control | Git |
| Remote Repository | GitHub |
| Data Format | JSON |
| File Encoding | UTF-8 |
| External Library | 사용하지 않음 |

### 버전 확인

```bash
python --version
git --version
```

실제 설치 버전:

- Python: [실제 버전 입력]
- Git: [실제 버전 입력]
- VS Code: [실제 버전 입력]

---

## 4. 주요 기능

### ① 퀴즈 풀기

- 등록된 항공·공항 퀴즈 출제
- 4개 선택지 제공
- 정답 및 오답 확인
- 최종 점수 계산
- 최고 점수 갱신 및 저장

### ② 퀴즈 추가

- 새로운 문제 등록
- 선택지 4개 입력
- 정답 번호 1~4 입력
- 입력값 검증
- JSON 파일에 자동 저장

### ③ 퀴즈 목록

- 등록된 전체 퀴즈 확인
- 문제 번호 및 문제 내용 출력
- 퀴즈가 없는 경우 안내

### ④ 점수 확인

- 최고 점수 확인
- 아직 게임을 진행하지 않은 경우 안내
- 새로운 최고 점수 자동 갱신
- JSON 파일에 점수 저장

### ⑤ 프로그램 종료

- 안전하게 프로그램 종료
- 데이터 저장 상태 확인
- Ctrl+C 및 입력 종료 상황 처리

---

## 5. 프로그램 메뉴 구성

```text
========================================
       ✈️ Aviation Quiz Game ✈️
========================================

1. 퀴즈 풀기
2. 퀴즈 추가
3. 퀴즈 목록
4. 점수 확인
5. 종료

========================================
메뉴를 선택하세요:
```

---

## 6. Python 프로그램 구조

### Quiz 클래스

개별 퀴즈 문제를 관리하는 클래스이다.

주요 속성:

- question: 문제 내용
- choices: 4개의 선택지
- answer: 정답 번호

주요 메서드:

- show_question(): 문제 출력
- check_answer(): 정답 확인

### QuizGame 클래스

퀴즈 게임 전체를 관리하는 클래스이다.

주요 속성:

- quizzes: 퀴즈 목록
- best_score: 최고 점수

주요 메서드:

- show_menu(): 메뉴 표시
- play_quiz(): 퀴즈 진행
- add_quiz(): 퀴즈 추가
- show_quizzes(): 퀴즈 목록 확인
- show_score(): 점수 확인
- save_data(): JSON 데이터 저장
- load_data(): JSON 데이터 불러오기
- run(): 프로그램 실행

---

## 7. 기본 퀴즈 데이터

프로젝트에 항공·공항 관련 기본 퀴즈 5개 이상을 포함한다.

예시 문제:

| 번호 | 문제 | 정답 |
|---|---|---|
| 1 | 항공기가 이륙할 때 주로 이용하는 시설은? | 활주로 |
| 2 | 항공기의 비행 방향을 조종하는 주요 장치는? | 방향타 |
| 3 | 공항에서 항공기와 승객이 이동하는 공간은? | 계류장 및 터미널 |
| 4 | 비행 중 항공기의 고도를 확인하는 장비는? | 고도계 |
| 5 | 항공기 운항을 관제하는 기관의 주요 업무는? | 항공교통관제 |

※ 실제 프로그램에는 문제, 선택지 4개, 정답 번호를 모두 포함하여 작성한다.

---

## 8. JSON 데이터 저장

프로젝트 루트 디렉토리에 `state.json` 파일을 생성한다.

### 데이터 저장 구조

```json
{
  "quizzes": [
    {
      "question": "항공기가 이륙할 때 이용하는 시설은?",
      "choices": [
        "주기장",
        "활주로",
        "터미널",
        "관제탑"
      ],
      "answer": 2
    }
  ],
  "best_score": 1
}
```

### JSON 파일 설명

| 항목 | 설명 |
|---|---|
| quizzes | 전체 퀴즈 데이터 |
| question | 문제 내용 |
| choices | 4개의 선택지 |
| answer | 정답 번호 |
| best_score | 최고 정답 개수 |

### 데이터 관리 방식

- UTF-8 인코딩으로 저장
- JSON 파일 읽기 및 쓰기
- 파일이 없으면 기본 퀴즈 사용
- JSON 데이터 손상 시 오류 안내
- 기본 퀴즈 데이터로 복구
- 프로그램 재실행 후 기존 데이터 유지

### 데이터 검증

1. 프로그램 실행
2. 새로운 퀴즈 추가
3. 프로그램 종료
4. 다시 프로그램 실행
5. 추가한 퀴즈 확인
6. 최고 점수 유지 여부 확인

---

## 9. 실행 방법

### 9-1. Python 설치 확인

```bash
python --version
```

Python 3.10 이상을 사용한다.

### 9-2. GitHub 프로젝트 복제

```bash
git clone https://github.com/본인계정/python-aviation-quiz-game.git
```

### 9-3. 프로젝트 디렉토리 이동

```bash
cd python-aviation-quiz-game
```

### 9-4. 프로그램 실행

```bash
python main.py
```

### 9-5. 종료

메뉴에서 5번을 선택한다.

---

## 10. 파일 구조

```text
python-aviation-quiz-game/
│
├── main.py
│   └── 프로그램 시작점
│
├── quiz.py
│   └── Quiz 클래스 정의
│
├── quiz_game.py
│   └── QuizGame 클래스 정의 및 게임 관리
│
├── state.json
│   └── 퀴즈 및 최고 점수 저장
│
├── README.md
│   └── 프로젝트 설명서
│
├── .gitignore
│   └── Git 제외 파일 설정
│
└── docs/
    └── screenshots/
        ├── menu.png
        ├── play.png
        ├── add_quiz.png
        ├── quiz_list.png
        ├── score.png
        └── git_log.png
```

---

## 11. 예외 처리

프로그램의 안정적인 실행을 위해 다음 예외 상황을 처리한다.

| 예외 상황 | 처리 방법 |
|---|---|
| 빈 입력 | 안내 메시지 출력 후 재입력 |
| 문자 입력 | 숫자 변환 오류 처리 |
| 범위 밖 입력 | 허용 범위 안내 |
| 퀴즈 없음 | 퀴즈가 없다는 안내 |
| JSON 파일 없음 | 기본 퀴즈 사용 |
| JSON 파일 손상 | 안내 후 기본 데이터 복구 |
| 파일 읽기 오류 | 오류 메시지 출력 |
| 파일 쓰기 오류 | 저장 실패 안내 |
| Ctrl+C | 저장 시도 후 안전 종료 |
| EOFError | 가능한 범위에서 저장 후 종료 |

주요 예외 처리 방법:

```python
try:
    number = int(input("번호 입력: ").strip())
except ValueError:
    print("숫자를 입력해주세요.")
except (KeyboardInterrupt, EOFError):
    print("프로그램을 안전하게 종료합니다.")
```

---

## 12. Git 버전 관리 및 커밋 기록

본 프로젝트는 기능 단위로 Git 커밋을 진행하여 개발 과정을 기록한다.

### 커밋 계획

| 번호 | 작업 내용 | 커밋 메시지 |
|---|---|---|
| 1 | 프로젝트 초기 설정 | Init: 프로젝트 생성 |
| 2 | README 작성 | Docs: 프로젝트 소개 작성 |
| 3 | Python 기본 파일 생성 | Feat: 프로그램 기본 구조 생성 |
| 4 | 메뉴 기능 구현 | Feat: 메인 메뉴 구현 |
| 5 | Quiz 클래스 구현 | Feat: Quiz 클래스 작성 |
| 6 | 기본 퀴즈 데이터 | Feat: 항공 퀴즈 5개 등록 |
| 7 | 퀴즈 풀기 | Feat: 퀴즈 출제 기능 구현 |
| 8 | 퀴즈 추가 | Feat: 퀴즈 등록 기능 구현 |
| 9 | 퀴즈 목록 | Feat: 퀴즈 목록 기능 구현 |
| 10 | 점수 확인 | Feat: 최고 점수 기능 구현 |
| 11 | JSON 저장 | Feat: JSON 데이터 저장 기능 구현 |
| 12 | 예외 처리 | Fix: 사용자 입력 예외 처리 |
| 13 | 클래스 구조 정리 | Refactor: 게임 클래스 구조 개선 |
| 14 | README 최종 수정 | Docs: 실행 방법 및 결과 추가 |

※ 위 내용은 커밋 계획이며, 실제 커밋 기록과 일치하도록 수정한다.

### 주요 Git 명령어

```bash
git init
git add .
git commit -m "Init: 프로젝트 생성"
git branch
git checkout -b feature/quiz-play
git checkout main
git merge feature/quiz-play
git push
git pull
git clone 저장소주소
```

### 브랜치 작업

퀴즈 풀기 기능은 별도 브랜치에서 작업한다.

```bash
git checkout -b feature/quiz-play
```

기능 구현 후 커밋한다.

```bash
git add .
git commit -m "Feat: 퀴즈 출제 기능 구현"
```

main 브랜치로 이동한다.

```bash
git checkout main
```

기능 브랜치를 병합한다.

```bash
git merge feature/quiz-play
```

### Git 커밋 이력 확인

```bash
git log --oneline --graph --all
```

---

## 13. Clone 및 Pull 실습

### Clone

GitHub 원격 저장소를 새로운 폴더에 복제한다.

```bash
git clone https://github.com/본인계정/python-aviation-quiz-game.git
```

### README 수정

복제한 프로젝트의 README.md에 학습 기록 한 줄을 추가한다.

### Commit 및 Push

```bash
git add README.md
git commit -m "Docs: clone 실습 기록 추가"
git push origin main
```

### 기존 프로젝트에서 Pull

처음 개발한 프로젝트 폴더로 이동한다.

```bash
git pull origin main
```

### 검증

기존 프로젝트의 README.md에 복제한 저장소에서 수정한 내용이 반영되었는지 확인한다.

---

## 14. 프로그램 실행 결과

실제 프로그램 실행 화면을 캡처하여 아래 경로에 저장한다.

### 메뉴 화면

`docs/screenshots/menu.png`

### 퀴즈 풀기

`docs/screenshots/play.png`

### 퀴즈 추가

`docs/screenshots/add_quiz.png`

### 퀴즈 목록

`docs/screenshots/quiz_list.png`

### 점수 확인

`docs/screenshots/score.png`

### Git 커밋 이력

`docs/screenshots/git_log.png`

---

## 15. 학습 결과 및 느낀 점

이번 프로젝트를 통해 Python의 기본 문법을 실제 프로그램에 적용하는 방법을 학습하였다.

변수와 자료형, 조건문, 반복문, 함수의 역할을 이해하고 이를 활용하여 메뉴 기반 퀴즈 게임을 구현하였다.

Quiz와 QuizGame 클래스를 분리하여 객체 지향 프로그래밍의 기본 구조를 경험하였으며, JSON 파일을 통해 프로그램의 데이터가 종료 후에도 유지되는 원리를 학습하였다.

또한 Git의 add, commit, push, pull, clone 및 checkout 명령어를 직접 사용하고 브랜치를 생성하고 병합하면서 버전 관리의 중요성을 이해하였다.

앞으로 Python을 활용한 데이터 분석과 자동화, 웹 개발 등으로 학습 범위를 확장하고자 한다.

---

## 16. 최종 제출 정보

- 프로젝트명: Aviation Quiz Game
- 과정: 개발 입문
- 학습시간: 40시간
- 과제명: 컴퓨터에게 명령 내리는 말(파이썬) 처음 배우기
- GitHub Repository: [저장소 주소 입력]
- Python Version: [실제 버전 입력]
- 작성자: [이름 또는 닉네임]
- 제출일: [실제 날짜 입력]

---

## 17. 최종 제출 체크리스트

- [ ] Python 프로그램 정상 실행
- [ ] Quiz 클래스 구현
- [ ] QuizGame 클래스 구현
- [ ] 기본 퀴즈 5개 이상 등록
- [ ] 퀴즈 풀기 기능
- [ ] 퀴즈 추가 기능
- [ ] 퀴즈 목록 기능
- [ ] 최고 점수 확인 기능
- [ ] JSON 저장 및 불러오기
- [ ] 프로그램 재실행 후 데이터 유지
- [ ] 입력값 및 예외 처리
- [ ] Git 의미 있는 커밋 10개 이상
- [ ] 브랜치 생성 및 병합
- [ ] Git clone 실습
- [ ] Git pull 실습
- [ ] README.md 작성
- [ ] 실행 결과 스크린샷
- [ ] GitHub 최종 업로드

**GitHub Repository:** [본인 저장소 주소]
