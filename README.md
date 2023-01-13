I need to get ServiceNow instance.  will store in $ServiceNowInstance

I need to get ServiceNow table. that is $ServiceNowInstance/someting/someting 



I need to write code according to above parameter 

we can also make flow chart in ServiceNow





$CI = 
If (Test-Connection -ComputerName $CI -Quiet -eq true)
        {
              $CI | Out-File -FilePath C:\temp\server.txt -Append
}



===========================================================================================================================================================

# This Below script we have to schedule in Task scheduler

$Date = Get-Date -DisplayHint Date 
$EmailFrom = “fiservservice@servicenow.fiserv.com”
$EmailTo = “FTS_TechOps_Distributed_T1@fiserv.com”
$Subject = “$Date closed INC's”
$Body = “Please find attached INC's close for today”
$SMTPServer = “smtp.outlook.com”   # we have to modify it for SNOW server
$Creds = (Get-Credential -Credential "$EmailFrom")



Send-MailMessage -To $EmailTo -From $EmailFrom -Subject $Subject -Body $Body -SmtpServer $SmtpServer -Attachment "server.txt"  -Credential $Creds -UseSsl  -Port 587






=============================================================================================================================================


$Date = Get-Date -DisplayHint Date 
$EmailFrom = “vs01121994@gmail.com”
$EmailTo = “vs01121994@gmail.com”
$Subject = “$Date closed INC's”
$Body = “Please find attached INC's close for today”
$SmtpServer = “smtp.gmail.com”
$Creds = (Get-Credential -Credential "$EmailFrom")



Send-MailMessage -To $EmailTo -From $EmailFrom -Subject $Subject -Body $Body -SmtpServer $SmtpServer -Credential $Creds -UseSsl  -Port 587



====================================================================================================================================================
