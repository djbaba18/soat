<?php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';
//Diqqat bu joyni o'zgartirishingizni keragi yoq xech qayerda korinmaydi shunchakiy
//Manba yoqolmasligi uchun mualiflik xuquqi buzilmasin 
//Bu rolik @YuRaKqOn tomonidan tayyorlab chiqildi 
$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();
$vaqt = date("H:i",strtotime("2 hour"));
$kun = date('d/m/y');
$MadelineProto->account->updateProfile(['about'=>"$vaqt  oxirgi kirilgan vaqt⏰  "]);
?>
