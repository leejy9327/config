session_set_cookie_params(0, "/");
ini_set("session.cookie_domain","");
ini_set("session.gc_maxlifetime", "86400");
session_start();
session_register($_SESSION['ss_num']);

if($_SESSION['ss_num'] == ""){
	echo "<script>alert('로그인 후에 이용하세요.');location.replace('../');</script>";
	exit;
}
