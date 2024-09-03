# NewsAPI
## 1. Everything
### URL : https://newsapi.org/v2/everything?
### Parameter
- **apiKey** : 본인의 api키, 필수항목
- **q** : 키워드

  - 정확하게 일치하는 키워드를 검색하려면 “”를 사용 

  - 반드시 표시되어야 하는 키워드는 +사용 ex) +keyword

  - 제외하고 싶은 키워드는 -사용 ex) -keyword

  - AND / OR / NOT을 사용하여 괄호로 그룹화할 수 있음 
  
  ex) crypto AND (ethereum OR litecoin) NOT bitcoin.

  q의 전체 값은 URL인코딩이 되어야 하며, 500자를 넘을 수 없다.

- **searchin** : 키워드의 검색필드

  - title

  - description

  - content
  
  여러 옵션을 쉼표로 구분해 검색할 수 있으며, 기본값은 모든 필드에 대해 검색을 수행

- **sources** : 헤드라인을 가져올 뉴스 소스 또는 블로그의 식별자를 쉼표로 구분한 문자열
- **domains** : 검색할 도메인을 지정하며, 쉼표로 구분하여 여러 도메인을 사용가능
- **excludeDomains** : 결과에서 제외할 도메인을 지정하며, 쉼표로 구분하여 사용가능
- **from** : 날짜 검색 시 시작 시점을 지정하며, ISO 8601 형식으로 입력해야 함
ex) 2024-09-03 또는 2024-09-03T02:33:46
- **to** : 날짜 검색 시 종료 시점을 지정하며, ISO86012 형식으로 입력해야 함
ex) 2024-09-03 또는 2024-09-03T02:33:46
- **language** : 헤드라인을 받을 언어의 2자리 ISO-639-1코드
가능한 옵션 :  ar, de, en, es, fr, he, it, nl, no, pl, pt, ru, sv, ud, zh.
- **sortBy** : 기사의 정렬 순서를 지정
- relevancy : q(키워드)와 더 밀접하게 관련된 기사가 먼저 나옴
- popularity : 인기 있는 출처 및 게시자의 기사가 먼저 나옴
- publishedAt : 최신 기사가 먼저 나옴
- **pageSize** : 페이지당 반환할 결과의 수로 기본값 : 100, 최대값 : 100
- **page** : 결과를 페이지별로 이동할 때 사용하며 기본값은 : 1
## 2. Top headlines
### url : https://newsapi.org/v2/top-headlines?
### Parameter
- **apiKey** : 본인의 api키, 필수 항목
- **country** : 검색할 국가의 2자리  ISO 3166-1 코드
가능한 옵션 : a, e, ar, at, au, be, bg, br, ca, ch, cn, co, cu, cz, de, eg, fr, gb, gr, hk, id, ie, il, in, it, jp, kr, lt, lv, ma, mx, my, ng, nl, no, nz, ph, pl, pt, ro, ru, sa, sg, sk, th, tr, tw, ua, us, ve, za
주의 : sources 매개변수와 같이 사용할 수 없음
- **category** : 검색할 카테고리
가능한 옵션 : business (비즈니스), entertainment (오락), general (일반), health (건강), **science** (과학), sports (스포츠), technology (기술)
주의 : sources 매개변수와 같이 사용할 수 없음
- **sources** : 헤드라인을 가져올 뉴스 소스 또는 블로그의 식별자를 쉼표로 구분한 문자열
               country 또는 category와 같이 사용할 수 없음
- **q** : 검색할 키워드
- **pageSize** : 페이지 당 반환할 결과의 수로 기본값은 20, 최대값은 100
- **page** : 총 결과 수가 페이지 크기보다 클 경우, 결과를 페이지별로 이동할 때 사용
