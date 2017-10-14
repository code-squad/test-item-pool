

# 시작하기
- iOS - Single View App 템플릿으로 시작하세요.
- 아래 요구사항을 만족하는 앱을 완성하세요.
- 본인 github에 저장소를 새로 만들고 문제 해결 과정을 단계별로 커밋 메시지에 기록하세요.
- 맨 아래 셀프 체크리스트를 꼭 추가하세요.

### 요구사항1. 데모 이미지를 프로젝트에 추가하세요.
- 데모 이미지 파일을 다운받으세요.
https://www.dropbox.com/s/3n0ip892eq3lytp/Demo%20Images.zip?dl=0
- 압축을 풀고 프로젝트 번들에 드래그 해서 추가하세요
- 프로젝트에 그룹을 만들어서 관리하면 편합니다

### 요구사항2. JSON 데이터

- 모델 객체 인스턴스를 만들고 
- 아래의 jsonString 데이터를 넘겨서
- Array 데이터를 title 기준으로 정렬시켜 사용하세요

```swift
let jsonString = """
[{\"title\":\"초록\",\"image\":\"01.jpg\",\"date\":\"20150116\"},
{\"title\":\"장미\",\"image\":\"02.jpg\",\"date\":\"20160505\"},
{\"title\":\"낙엽\",\"image\":\"03.jpg\",\"date\":\"20141212\"},
{\"title\":\"계단\",\"image\":\"04.jpg\",\"date\":\"20140301\"},
{\"title\":\"벽돌\",\"image\":\"05.jpg\",\"date\":\"20150101\"},
{\"title\":\"바다\",\"image\":\"06.jpg\",\"date\":\"20150707\"},
{\"title\":\"벌레\",\"image\":\"07.jpg\",\"date\":\"20140815\"},
{\"title\":\"나무\",\"image\":\"08.jpg\",\"date\":\"20161231\"},
{\"title\":\"흑백\",\"image\":\"09.jpg\",\"date\":\"20150102\"},
{\"title\":\"나비\",\"image\":\"10.jpg\",\"date\":\"20141225\"}]
"""
```

### 요구사항3. Album ViewController 구현하기
- TableView DataSource를 Album ViewController로 설정
- TableView에 Model에 있는 10개 데이터를 출력하세요
- `func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell` 델리게이트 메서드를 구현하세요
- `cell.titleLabel` 에는 title 을 표시하고, `cell.detailLabel` 에는 date를 표시하세요
- `cell.backgroundImage` 에 이미지를 center로 alignment 해서 표시하세요.

![Tableview](http://public.codesquad.kr/jk/tableView-cell.png)

### 요구사항4. Photo ViewController 구현하기
- TableView에서 row를 select 하면 다음 화면을 보여주세요. 
- Image는 원래 비율(aspect fit)로 보여주세요.

![PhotoViewController](http://public.codesquad.kr/jk/photo-ViewController.png)

### 요구사항5. TableView Header
- 날짜순으로 정렬한 상태의 년도별로 Section을 나눠서 표시하고 Header에 년도를 표시하세요.

![TableviewHeader](http://public.codesquad.kr/jk/tableView-header.png)

## 셀프 체크리스트
- 프로젝트에 checklist.md 파일을 추가하고 아래 항목을 복사해서 붙여넣으세요.
- 아래 항목에 대해 자신의 경험을 체크하고, 자신의 점수를 각 10점만점 기준으로 적고, 그 이유를 주관식으로 문장으로 쓰세요.

[항목#1] 스위프트(또는 Objective-C) 언어로 여러 가지 상황별 주어진 문제를 해결하는 경험

- 1-1 Immutable 객체와 Mutable 객체의 차이를 이해하고 설명할 수 있다.
- 1-2 특정 디렉터리에 있는 파일 목록을 탐색하는 알고리듬을 구현할 수 있다.
- 1-3 C 혹은 Objective-C 데이터 타입을 스위프트 구조체로 바꾸거나 클래스로 표현하여 Collection 객체에 담아 저장할 수 있다.
- 1-4 주어진 상황에 맞게 Array나 Dictionary에 담겨있는 데이터를 탐색하고 정렬할 수 있다. (JSON 처리 등) 
- 1-5 자동/수동 메모리 관리 방법을 구분하고 차이점을 설명할 수 있다.

자기 의견: 

[항목#2] 인터페이스 디자인 가이드(HIG)를 기초로 기본 UI Control 동작을 구현하는 경험

- 2-1 스토리보드 상에 ViewController 단위로 화면을 디자인하고 Segue로 전환할 수 있다.
- 2-2 UITableView 에 Custom Cell 형태로 디자인하고 DataSource Delegate 메서드를 구현할 수 있다.
- 2-3 메모리 효율을 위해 화면에 보이지 않는 객체를 해제하는 LRU 형태 캐시를 구현할 수 있다.
- 2-4 MVC 패턴을 이해하고 각각 역할에 맞는 클래스를 구현하고 Notification을 보내는 구조를 구현할 수 있다.

자기 의견: 

[항목#3] iOS 앱 개발을 위해 프레임워크 API를 활용하는 경험  

- 3-1 네트워크 처리 및 Async 방식 이벤트 처리 기술을 적용할 수 있다. 
- 3-2 Core Graphics 방식으로 커스텀 그래프 컨트롤을 만들 수 있다. 
- 3-3 Transition 형태의 뷰 애니메이션을 직접 만들 수 있다. 
- 3-4 서버와 통신하기 위한 HTTP 또는 TCP 방식의 통신 모듈을 만들 수 있다. 
- 3-5 Block과 GCD (또는 Operation Queue)를 이용한 비동기 방식으로 작업 스케줄링을 구현 수 있다. 

자기 의견: 

[항목#4] iOS 개발 환경을 이용해서 프로젝트를 관리하고 프로파일링하는 경험

- 4-1 Xcode 도구를 이용해 iOS 프로젝트를 관리하고 실제 기기에 설치/배포할 수 있다. 
- 4-2 Instruments 도구를 이용해서 앱 프로파일링 분석하고, 코드를 개선할 수 있다. 
- 4-3 Xcode로 만든 프로젝트를 소스관리 저장소에서 관리할 수 있다.

자기 의견: 