session_set_cookie_params(0, "/");
ini_set("session.cookie_domain","");
ini_set("session.gc_maxlifetime", "86400");
session_start();
session_register($_SESSION['ss_num']);
$_SESSION은 php4.1 이후 버젼에서 사용가능 합니다. 그 전 버젼은
session_register() 함수를 사용 하셔야 합니다. 

if($_SESSION['ss_num'] == ""){
	echo "<script>alert('로그인 후에 이용하세요.');location.replace('../');</script>";
	exit;
}
