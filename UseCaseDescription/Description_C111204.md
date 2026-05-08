# 온라인 설문조사 플랫폼 Use Case Description

## 1. 개요

본 문서는 온라인 설문조사 플랫폼의 Use Case Description을 정리한다.

---

## 2. Use Case Description

#### Use Case Description: 회원가입
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '회원가입' 버튼 클릭</td>
    <td>2. 회원가입 화면으로 전환</td>
  </tr>
  <tr>
    <td>3. 필수 입력 정보(ID, 비밀번호, 이름, 전화번호, 메일 등)를 입력하고 '저장' 버튼 클릭</td>
    <td>4. 입력된 데이터의 유효성을 검증 후 DB에 해당 데이터를 저장 후, 가입 성공 화면 출력 후 자동으로 로그인 화면으로 전환</td>
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      1a. 로그인 상태: System은 '회원가입' 버튼 비활성화<br>
      3a. 필수 입력 정보 누락: System은 누락된 항목을 강조하고, '필수 항목을 모두 입력해주세요' 메시지 출력<br>
      3b. ID 중복: System은 '이미 사용 중인 ID입니다' 메시지 출력
    </td>
  </tr>
</table>

#### Use Case Description: 회원 탈퇴
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '회원 탈퇴' 버튼 클릭</td>
    <td>2. 회원 탈퇴 페이지로 전환 후, 탈퇴 안내 및 주의사항 출력</td> 
  </tr>
  <tr>
    <td>3. '확인(탈퇴)' 버튼 클릭</td>
    <td>4. 회원의 모든 이용권한과 데이터 삭제 후, '탈퇴가 완료되었습니다' 메시지와 함께 메인 화면으로 이동</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      1a. 로그아웃 상태: '회원 탈퇴' 버튼 비활성화<br>
      1b. 관리자 로그인: '회원 탈퇴' 버튼 비활성화
    </td>
  </tr>
</table>

#### Use Case Description: 설문 검색
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '설문 검색' 버튼 클릭</td>
    <td>2. 설문 검색 페이지로 이동</td> 
  </tr>
  <tr>
    <td>3. 현재 진행 중인 설문 리스트, 향후 진행 예정인 설문 리스트, 종료된 설문 리스트 중 하나를 선택한 후 키워드를 입력하여 검색</td>
    <td>4. 조건에 맞는 설문 리스트 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      3a. 검색 결과가 없는 경우: System은 '조건에 맞는 검색 결과가 없습니다' 메시지 출력
    </td>
  </tr>
</table>

#### Use Case Description: 상세정보 조회[회원]
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. 설문 리스트 화면에서 특정 설문 선택</td>
    <td>2. 새 화면에서 상세 정보(설문 제목, 설문 설명, 설문 문항, 응답 항목, 설문 시작 시각, 설문 마감 시각 등) 출력 후, '응답' 버튼 활성화</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      2a. 현재 진행 중인 설문이 아닌 경우: System은 '응답' 버튼 비활성화
    </td>
  </tr>
</table>

#### Use Case Description: 설문 응답
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '응답' 버튼 클릭</td>
    <td>2. 응답 화면으로 이동</td> 
  </tr>
  <tr>
    <td>3. 응답 후 '응답(제출)' 버튼 클릭</td>
    <td>4. 응답 데이터를 DB에 저장 후, '응답이 완료되었습니다' 메시지 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      3a. 미응답 문항 존재: '응답(제출)' 버튼 비활성화
    </td>
  </tr>
</table>

#### Use Case Description: 응답 설문 조회
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '내 응답 조회' 버튼 클릭</td>
    <td>2. 회원이 응답한 모든 설문 정보(설문 제목, 응답 내용, 응답 일시 등)를 새 화면에 출력</td>
  </tr>
  <tr>
    <td colspan="2">
      <strong>Extensions</strong><br>
      E1. 응답 취소<br>
      &emsp;1. [Actor] 회원이 설문 리스트에서 '취소' 버튼 클릭<br>
      &emsp;2. [System] '응답 데이터가 삭제됩니다. 정말 취소하시겠습니까?' 경고 팝업 출력<br>
      &emsp;3. [Actor] 회원이 '확인' 버튼 클릭<br>
      &emsp;4. [System] 해당 응답 데이터를 DB에서 삭제 후, '삭제되었습니다' 알림과 함께 갱신된 조회 리스트 출력
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      1a. 응답한 설문이 없는 경우: System은 '응답한 설문 내역이 없습니다' 안내 출력<br>
      2a. 설문이 종료된 경우: System은 해당 설문 항목의 '취소' 버튼을 비활성화<br>
      E2-3a. 삭제 취소: System은 데이터 변경 없이 팝업을 닫고 기존 리스트 화면 유지
    </td>
  </tr>
</table>

#### Use Case Description: 응답 수정
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. 설문 리스트에서 '수정' 버튼 클릭</td>
    <td>2. 설문 수정 화면으로 이동, 가장 최근에 수정한 날짜도 함께 출력</td> 
  </tr>
  <tr>
    <td>3. 수정할 데이터 입력 후 '수정(제출)' 버튼 클릭</td>
    <td>4. 수정된 데이터 DB에 반영 후 '수정이 완료되었습니다' 메시지 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      1a. 설문이 종료된 경우: System은 '수정' 버튼 비활성화<br>
      3a. 필수 항목 누락: 회원이 필수 문항의 답변을 지우고 제출 시도 시, System은 저장을 거부하고 누락된 항목을 강조하여 표시<br>
      3b. 변경 내용 없음: System은 DB 업데이트를 생략하고 '변경된 내용이 없습니다' 메시지 출력
    </td>
  </tr>
</table>

#### Use Case Description: 로그인
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '로그인' 버튼을 클릭</td>
    <td>2. 로그인 화면으로 전환</td> 
  </tr>
  <tr>
    <td>3. ID와 비밀번호를 입력하고 '로그인' 버튼을 클릭</td>
    <td>4. 등록된 회원 정보와 일치하는지 확인 후, 메인 화면으로 이동</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      1a. 로그인 상태: System은 '로그인' 버튼 비활성화<br>
      3a. 정보 불일치: System은 'ID 또는 비밀번호가 일치하지 않습니다' 출력
    </td>
  </tr>
</table>

#### Use Case Description: 로그아웃
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '로그아웃' 버튼 클릭</td>
    <td>2. 현재 세션 종료 후, 사용자를 메인 화면(또는 로그인 화면)으로 이동</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      1a. 비로그인 상태: System은 '로그아웃' 버튼 비활성화
    </td>
  </tr>
</table>

#### Use Case Description: 설문 등록
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '설문 등록' 버튼 클릭</td>
    <td>2. 설문 등록 화면으로 이동</td> 
  </tr>
  <tr>
    <td>3. 필요 정보(설문 제목, 설문 설명, 설문 문항, 응답 항목, 설문 시작 시각, 설문 마감 시각 등) 입력 후 '등록' 버튼 클릭</td>
    <td>4. 새로운 설문을 DB에 저장 후, '설문 등록이 완료되었습니다' 메시지 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      3a. 필드 누락: System은 '입력되지 않은 필드가 있습니다' 출력<br>
      3b. 시간 오류: 설문 마감 시각이 과거거나, 마감 시각이 시작 시각보다 빠른 경우, System은 '시간 설정이 올바르지 않습니다' 출력
    </td>
  </tr>
</table>

#### Use Case Description: 설문 조회
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td>1. '등록 설문 조회' 버튼 클릭</td>
    <td>2. 화면 전환 후, 등록된 모든 설문 리스트 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Extensions</strong><br>
      E1. 상세정보 조회[관리자]<br>
      &emsp;1. [Actor] 관리자가 특정 설문 항목 클릭<br>
      &emsp;2. [System] 해당 설문 항목의 상세 내용을 팝업 창으로 출력<br>
      E2. 설문 삭제<br>
      &emsp;1. [Actor] 관리자가 특정 설문 항목의 '삭제' 버튼 클릭<br>
      &emsp;2. [System] '설문이 삭제됩니다. 정말 삭제하시겠습니까?' 경고 팝업 출력<br>
      &emsp;3. [Actor] 관리자가 '확인' 버튼 클릭<br>
      &emsp;4. [System] 해당 설문을 DB에서 지우고 갱신된 리스트를 출력
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      E2-3a. 삭제 취소: System은 데이터 변경 없이 팝업을 닫고 기존 리스트 화면 유지
    </td>
  </tr>
</table>

#### Use Case Description: 설문 통계 조회
<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>  
    <td>1. '설문 통계 조회' 버튼 클릭</td>
    <td>2. 화면 전환 후, 검색 단위(최근 1주일, 1개월, 1년 중) 선택지와 '조회' 버튼 등 출력</td> 
  </tr>
  <tr>  
    <td>3. 검색 단위 선택 후, '조회' 버튼 클릭</td>
    <td>4. 선택된 기간 동안의 전체 설문 수, 종료된 설문 수, 총 응답 수 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      None.
    </td>
  </tr>
</table>
