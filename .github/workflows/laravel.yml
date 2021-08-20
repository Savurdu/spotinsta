<?php
session_start();

require_once '../vendor/instagram-private-api-php/Instagram.php';
require_once 'Settings.php';

error_reporting(0);


$username = 'harun.t0';

$password = '191202zeki1';

$sizinemailiniz = 'savurduuuu@gmail.com';

$debug = false;

if($_GET['Status'] == "Ok"){
    if($_SESSION['Value'] != null){
        $i = new Instagram($username,$password);

        $i->login();

        $editProfile = $i->editProfile("","","",$_SESSION['Value'],"$sizinemailiniz",1);

        if($editProfile['status'] == "fail"){
            echo 'Bir Hata Oluştu !';
        }
        if($editProfile['status'] == "ok"){
            echo 'Biyografi Başarı İle Güncelleşti !';
            header("Refresh:2; url=WaitBiography.php?wait=21");
        }
    } else{
        echo 'Bir Hata İle Karşılaştık !';
    }
} else{
    echo 'Yanlış Bir Sayfada Olabilirsiniz !';
}
