### 관계
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/995a7e35-3673-432a-981d-99e93dc06b89" />
</br>

수정하기 전
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/4469b469-c21b-4756-aacf-3843b707ff72" />
</br>

수정한 후
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/f3675a09-1b67-4683-afaa-8b0773fe13e7" />
</br>

Theater가 파는게 아닌데 Theater가 파는 것처럼 되어있으니까 줌(자율성)
theater를 티켓 셀러에 옮겼어 내부로 옮겨서 theater가 깔끔하게 바껴서 참조가 사라짐

Q. Theater가 Bag으로 끊긴건 get, set호출을 안하니까인가요?
판매자가 티켓을 판매하기 위해 TicketOffice를 사용하는 모든 부분을 TicketSeller 내부로 옮기고 관람객이 티켓을 구매하기 위해 Bag을 사용하는 모든 부분 Audience 내부로 옮긴 것이다.

서비스 implement 구현하는?

### 클린코드
if(object != null)의 습관적인 사용은 그만!

1. 프로그래밍 습관을 통한 NPE 예방 방법
 * equals(), equalsIgnoreCase() 비교 시 문자열이나 null이 아닌 객체를 선행하여 비교하자
 * toString() 보다는 String.valueOf()를 사용하자
 * 필요한 경우가 아니면 reference 타입보다는 primitive 타입을 사용하자 (wrpping class는 좀더 많은 메모리 공간을 차지하며 null에 대한 대비가 필요하다)
 * 함수에서 null 대신 빈 Collection 객체를 반환하자 (null을 반환하면 호출자는 그에 대비하여 null 확인 구문이 필요하다)
 * null에 안전한 자바 내장 함수나 commons-lang과 같은 helper class을 활용하자 
 * Java assert, Unit Test을 활용하여 논리적으로 발생이 불가한 상황에 대한 사전 확인과 다양한 상황에서의 테스트를 수행하자
