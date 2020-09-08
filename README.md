# XAMPP PHP VERSION SWITCHER

Prerequisite : XAMPP with php 5 should already installed and running fine

Goal : Implement multiple php versions i.e. php5, php7.1 and php7.2 in a single xampp installation

------------------------------------


STEP 1 : STOP Apache and MySQL server of XAMPP if they are running

STEP 2 : Download XAMPP 7z or zip version and extract, Reference link :  https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/

STEP 3 : Take php folder from extracted xampp downloaded in STEP 2 and place it into previously installed "xampp" directory by renaming the folder name (e.g. php71 for v7.1, php72 for v7.2). So there will be multiple php folders like "php", "php71", "php72" in the same location

STEP 4 : Copy "xampp\apache\conf\extra\httpd-xampp.conf" file from the installed "xampp" directory and place it into the same folder with a name like "xampp\apache\conf\extra\httpd-xampp71.conf" (for version 7.1), So now both httpd-xampp.conf & httpd-xampp71.conf are in same location

STEP 5 : Open "xampp\apache\conf\extra\httpd-xampp71.conf" and change all occurrence of "/xampp/php/" with "/xampp/php71/", "php5_module" with "php7_module", "php5apache2_4.dll" with "php7apache2_4.dll", "\\\\xampp\\\\php" with "\\\\xampp\\\\php71", "php5ts.dll" with "php7ts.dll"

STEP 6 : Open "xampp\php71\php.ini" and change all occurrence of "\xampp\php\" with "\xampp\php71\"

STEP 7 : Execute same stapes from STEP 2 to STEP 6 for php 7.2 (in this case folder name will be "php72" but all others like "php7_module", "php7apache2_4.dll" or "php7ts.dll" will stays same)

STEP 8 : Place this switcher folder anywhere in your machine

STEP 9 : Specify absolute path of installed "xampp" folder(e.g. c:\xampp\ , trailing slash should be there) in "php_switch\xampp_path.txt". You can find this file inside this tool. There should not be any other line in this txt file, after this folder path placement.

STEP 10 : Double click on phpSwitcher.bat and input as required
