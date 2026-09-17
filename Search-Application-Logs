Get-WinEvent -LogName "Application" -MaxEvents 300 |
    Where-Object {
        $_.ProviderName -eq "MsiInstaller"
    } |
    Where-Object {
        $_.TimeCreated -gt (Get-Date).AddMinutes(-15)
    } |
    Select-Object TimeCreated, Id, Message |
    Format-List
