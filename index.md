<?php

header('Refresh: 3;index.html');

$message = $_POST['name'] . PHP_EOL. $_POST['mobile'] . PHP_EOL. ($_POST['email'] . PHP_EOL. $_POST['message']);

if(isset($_POST['email'])){
	mail("Email@gmail.com","enquiry for a ~~~~!", $message);
	echo "Email Sent!";//to email, subject, message.
	echo "Redirecting...";
}
