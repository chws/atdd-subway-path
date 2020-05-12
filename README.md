# atdd-subway-path

## 1단계 - 캐시 적용

### 요구사항

- [ ] HTTP 캐시 적용하기
- [ ] HTTP Cache의 종류를 학습
- [ ] 지하철 노선도 조회 시 ETag를 통해 캐시를 적용
- [ ] LineControllerTest의 ETag 테스트를 성공 시키기

## 실습 - 지하철 노선도 조회

### 요구사항

- [x] 모든 지하철 노선과 각 노선에 포함된 지하철역 조회 기능 구현
- [x] 인수 테스트와 단위 테스트를 작성
- [x] 페이지 연동

### 기능 목록

- 지하철 노선도 페이지 조회
  - 모든 지하철 노선과 지하철역 목록을 조회

### 시나리오

```gherkin
Feature: 전체 지하철 노선도 정보 조회

  Scenario: 지하철 노선도 정보 조회를 한다.
    Given 지하철역이 여러 개 추가되어있다.
    And 지하철 노선이 여러 개 추가되어있다.
    And 지하철 노선에 지하철역이 여러 개 추가되어있다.
    
    When 지하철 노선도 전체 조회 요청을 한다.
    
    Then 지하철 노선도 전체를 응답 받는다.
```
