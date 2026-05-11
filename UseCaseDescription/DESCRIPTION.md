# Use Case Description

### Use Case Description: 회원가입

Primary Actor: 회원

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 회원가입 버튼 클릭</td>
    <td style="vertical-align: top;">2. 회원가입 화면 출력</td>
  </tr>
  <tr>
    <td style="vertical-align: top;">
      3.1. 필수 입력 정보(ID, 비밀번호, 이름, 전화번호, 이메일 등) 입력<br>
      3.2. 가입 버튼 클릭</td>
    <td style="vertical-align: top;">
      4.1. 입력된 정보의 유효성을 검증<br>
      4.2. 입력된 정보를 등록<br>
      4.3. 회원가입 완료 메시지 출력<br>
      4.4. 로그인 화면으로 전환
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      4.1a. 필수 입력 정보 누락: System은 누락된 항목을 강조하고, '필수 항목을 모두 입력해주세요' 메시지 출력<br>
      4.1b. ID 중복: System은 '이미 사용 중인 ID입니다' 메시지 출력
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 회원 탈퇴

Primary Actor: 회원

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. '회원 탈퇴' 메뉴 선택</td>
    <td style="vertical-align: top;">2. 회원 탈퇴 화면으로 전환</td> 
  </tr>
  <tr>
    <td style="vertical-align: top;">3. 탈퇴 버튼 클릭</td>
    <td style="vertical-align: top;">4. 탈퇴 확인 경고 메시지 출력</td>
  </tr>
  <tr>
    <td style="vertical-align: top;">5. 확인 버튼 클릭</td>
    <td style="vertical-align: top;">
      6.1. 회원의 모든 이용권한과 데이터 삭제<br>
      6.2. 탈퇴 완료 메시지 출력<br>
      6.3. 로그인 화면으로 이동</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      5a. 탈퇴 취소: System은 탈퇴 처리를 수행하지 않고 경고 메시지를 닫은 뒤 이전 화면 유지
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 설문 검색

Primary Actor: 회원

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 설문 검색 메뉴 클릭</td>
    <td style="vertical-align: top;">2. 설문 검색 화면 출력</td> 
  </tr>
  <tr>
    <td style="vertical-align: top;">
      3.1. 현재 진행 중인 설문 리스트, 향후 진행 예정인 설문 리스트, 종료된 설문 리스트 중 하나를 선택<br>
      3.2. 키워드를 입력<br>
      3.3. 검색 버튼 클릭</td>
    <td style="vertical-align: top;">4. 조건에 맞는 설문 리스트 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      4a. 검색 결과가 없는 경우: System은 '조건에 맞는 검색 결과가 없습니다' 메시지 출력
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 상세정보 조회[회원]

Primary Actor: 회원

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 검색 결과 설문 리스트 화면에서 특정 설문 선택</td>
    <td style="vertical-align: top;">
      2.1. 새 화면에서 상세 정보(설문 제목, 설문 설명, 설문 문항, 응답 항목, 설문 시작 시각, 설문 마감 시각 등) 출력<br>
      2.2. 현재 진행 중인 설문인 경우 응답 버튼 활성화
    </td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      2.2a. 현재 진행 중인 설문이 아닌 경우: System은 응답 버튼 비활성화
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 설문 응답

Primary Actor: 회원

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 응답 버튼 클릭</td>
    <td style="vertical-align: top;">2. 응답 화면 출력</td> 
  </tr>
  <tr>
    <td style="vertical-align: top;">
      3.1. 양식에 따라 응답 내용 작성<br>
      3.2. 응답 버튼 클릭
    </td>
    <td style="vertical-align: top;">
      4.1. 응답 내용 제출 처리<br>
      4.2. 응답 완료 메시지 출력
    </td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      4.1a. 미응답 문항 존재: System은 응답 제출 처리를 중단하고, 누락된 항목을 강조 표시
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 응답 설문 조회

Primary Actor: 회원

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 응답 설문 조회 버튼 클릭</td>
    <td style="vertical-align: top;">
      2.1. 회원이 응답한 모든 설문 정보(설문 제목, 응답 내용, 응답 일시 등)를 새 화면에 출력<br>
      2.2. 현재 진행 중인 항목에는 수정 버튼과 취소 버튼 활성화
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <strong>Extensions</strong><br>
      E1. 응답 취소<br>
      &emsp;1. [Actor] 회원이 응답 설문 조회 화면에서 현재 진행 중인 특정 설문의 취소 버튼 클릭<br>
      &emsp;2. [System] 취소 확인 경고 팝업 출력<br>
      &emsp;3. [Actor] 회원이 취소 확인 버튼 클릭<br>
      &emsp;4.1. [System] 해당 응답 취소 처리<br>
      &emsp;4.2. [System] 취소 완료 메시지 출력<br>
      &emsp;4.3. [System] 갱신된 조회 리스트 출력
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      2.1a. 응답한 설문이 없는 경우: System은 응답한 설문 내역이 없다는 안내 출력<br>
      2.2a. 설문이 종료된 경우: System은 해당 설문 항목의 수정 버튼과 취소 버튼을 비활성화<br>
      E1-3a. 응답 취소 철회: System은 데이터 변경 없이 팝업을 닫고 기존 리스트 화면 유지
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 응답 수정

Primary Actor: 회원

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 응답 설문 조회 화면에서 현재 진행 중인 특정 설문의 수정 버튼 클릭</td>
    <td style="vertical-align: top;">2. 가장 최근에 수정한 날짜와 함께 응답 수정 화면 출력</td> 
  </tr>
  <tr>
    <td style="vertical-align: top;">
      3.1. 수정할 데이터 입력<br>
      3.2. 수정 버튼 클릭
    </td>
    <td style="vertical-align: top;">
      4.1. 수정된 내용 반영<br>
      4.2. 수정 완료 메시지 출력
    </td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      4.1a. 필수 항목 누락: 회원이 필수 문항의 답변을 지우고 수정 시도 시, System은 수정 완료 처리를 중단하고 누락된 항목을 강조하여 표시<br>
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 로그인

Primary Actor: 회원, 관리자

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 로그인 버튼 클릭</td>
    <td style="vertical-align: top;">2. 로그인 화면 출력</td> 
  </tr>
  <tr>
    <td style="vertical-align: top;">
      3.1. ID와 비밀번호를 입력<br>
      3.2. 로그인 버튼을 클릭</td>
    <td style="vertical-align: top;">
      4.1. 등록된 회원 정보와 일치하는지 확인<br>
      4.2. 사용자 권한에 맞는 메인 화면으로 이동</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      4a. 정보 불일치: System은 오류 메시지 출력
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 로그아웃

Primary Actor: 회원, 관리자

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 로그아웃 버튼 클릭</td>
    <td style="vertical-align: top;">
      2.1. 로그아웃 상태로 전환<br>
      2.2. 로그인 화면으로 이동</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      None
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 설문 등록

Primary Actor: 관리자

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 설문 등록 버튼 클릭</td>
    <td style="vertical-align: top;">2. 설문 등록 화면 출력</td> 
  </tr>
  <tr>
    <td style="vertical-align: top;">
      3.1. 필요 정보(설문 제목, 설문 설명, 설문 문항, 응답 항목, 설문 시작 시각, 설문 마감 시각 등) 입력<br>
      3.2. 등록 버튼 클릭</td>
    <td style="vertical-align: top;">
      4.1. 입력된 데이터의 유효성 확인<br>
      4.2. 설문 정보 등록<br>
      4.3. 설문 등록 완료 메시지 출력
    </td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      4.1a. 필드 누락: System은 '입력되지 않은 필드가 있습니다' 출력<br>
      4.1b. 시간 오류: 설문 마감 시각이 과거거나, 마감 시각이 시작 시각보다 빠른 경우, System은 '시간 설정이 올바르지 않습니다' 출력
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 설문 조회

Primary Actor: 관리자

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>
    <td style="vertical-align: top;">1. 등록 설문 조회 메뉴 클릭</td>
    <td style="vertical-align: top;">2. 등록된 모든 설문 리스트 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Extensions</strong><br>
      E1. 상세정보 조회[관리자]<br>
      &emsp;1. [Actor] 관리자가 특정 설문 항목 클릭<br>
      &emsp;2. [System] 해당 설문 항목의 상세 내용을 팝업 창으로 출력<br>
      E2. 설문 삭제<br>
      &emsp;1. [Actor] 관리자가 특정 설문 항목의 삭제 버튼 클릭<br>
      &emsp;2. [System] 삭제 확인 경고 팝업 출력<br>
      &emsp;3. [Actor] 관리자가 확인 버튼 클릭<br>
      &emsp;4.1. [System] 해당 설문 삭제<br>
      &emsp;4.2. [System] 설문 삭제 완료 메시지 출력<br>
      &emsp;4.3. [System] 갱신된 설문 리스트 출력
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      2a. 등록 설문 없음: System은 등록된 설문이 없다는 메시지 출력<br>
      E2-3a. 삭제 취소: System은 데이터 변경 없이 팝업을 닫고 기존 리스트 화면 유지
    </td>
  </tr>
</table>
<hr>

### Use Case Description: 설문 통계 조회

Primary Actor: 관리자

<table width="100%">
  <tr>
    <th width="50%">Actor Action</th>
    <th width="50%">System Response</th>
  </tr>
  <tr>  
    <td style="vertical-align: top;">1. 설문 통계 조회 메뉴 클릭</td>
    <td style="vertical-align: top;">2. 검색 단위(최근 1주일, 1개월, 1년 중) 선택지와 조회 버튼이 있는 설문 통계 조회 화면 출력</td> 
  </tr>
  <tr>  
    <td style="vertical-align: top;">
      3.1. 검색 단위 선택<br>
      3.2. 조회 버튼 클릭
    </td>
    <td style="vertical-align: top;">4. 선택된 기간 동안의 전체 설문 수, 종료된 설문 수, 총 응답 수 출력</td> 
  </tr>
  <tr>
    <td colspan="2">
      <strong>Alternative Courses</strong><br>
      None
    </td>
  </tr>
</table>
