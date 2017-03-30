# binaryconversion
function that converts numbers to binary


   <?php
function convertBin($decimalNum)
{
 

 $binaryNum = '';  
 do
  {
   $binaryNum = bcmod($decimalNum,'2') . $binaryNum;
   $decimalNum = bcdiv($decimalNum,'2');
  } while (bccomp($decimalNum,'0'));

 return($binaryNum);
}
?>


<?php
echo convertBin('90'); 
?>
