
session_set_cookie_params(0, "/"); // 세션쿠키가 적용되는 위치 (특별한 경우가 없다면 일반적으로 홈디렉토리 루트경로인 / 를 설정합니다.) 
ini_set("session.cookie_domain", "세션이활성화될도메인"); 
ini_set("session.gc_maxlifetime", ""); // 사용자가 아무짓안할경우 마감한다 세션 만료시간 설정
// session.cache_expire 세션캐쉬 삭제되는 시간  분단위
웹브라우저를 끌때까지 생존한다 
//session.cookie_lifetime = 0
session_start();
//session_register($_SESSION['ss_num']);
//$_SESSION은 php4.1 이후 버젼에서 사용가능 합니다. 그 전 버젼은 session_register() 함수를 사용 하셔야 합니다.

if($_SESSION['user_code'] == ""){ echo "<script>alert('로그인 후에 이용하세요.');location.replace('../');</script>"; exit; }



