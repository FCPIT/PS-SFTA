PowerShell Set File/Protocol Type Association Default Application Windows 10/11

## Features
* Set File Type Association.
* Set Protocol Association.
* Get File Type Association.
* List File Type Association.
* Get Protocol Type Association.
* List Protocol Type Association.
* Register Application.
* Unregister Application.

## Basic Usage

##### Set Acrobat Reader DC as Default .pdf reader:
```powershell
Set-FTA AcroExch.Document.DC .pdf

```

##### Set Google Chrome as Default for http Protocol:
```powershell
Set-PTA ChromeHTML http

```

##### Register Application and Set as Default for .pdf reader:
```powershell
Register-FTA "C:\SumatraPDF.exe" .pdf -Icon "shell32.dll,100"

```

## Additional Instructions

##### Set Microsoft Edge as Default .pdf reader from Windows Command Processor (cmd.exe):
```powershell
powershell -ExecutionPolicy Bypass -command "& { . .\SFTA.ps1; Set-FTA 'MSEdgePDF' '.pdf' }"

```

##### Set Sumatra PDF as Default .pdf reader from Windows Command Processor (cmd.exe):
```powershell
powershell -ExecutionPolicy Bypass -command "& { . .\SFTA.ps1; Set-FTA 'Applications\SumatraPDF.exe' '.pdf' }"

```

##### Set Google Chrome as Default .csv reader from PowerShell (Load Script From GitHub Raw URL):
```powershell
powershell -ExecutionPolicy Bypass -command "& { [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/FCPIT/PS-SFTA/refs/heads/master/SFTA.ps1'));Set-FTA 'Applications\SumatraPDF.exe' '.pdf' }"

```
