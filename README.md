<div align="center">

## Desktop on form


</div>

### Description

Put your desktop on a form and be able to click programs to open them right from it...
 
### More Info
 
You have to restart / or \ log off computer afterwards to restore desktop


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Morpheous Dreams](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/morpheous-dreams.md)
**Level**          |Beginner
**User Rating**    |3.8 (15 globes from 4 users)
**Compatibility**  |VB 6\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/morpheous-dreams-desktop-on-form__1-47008/archive/master.zip)

### API Declarations

```
Private Declare Function FindWindow Lib "user32" Alias "FindWindowA" (ByVal lpClassName As String, ByVal lpWindowName As String) As Long
Private Declare Function FindWindowEx Lib "user32" Alias "FindWindowExA" (ByVal hWnd1 As Long, ByVal hWnd2 As Long, ByVal lpsz1 As String, ByVal lpsz2 As String) As Long
Private Declare Function SetParent Lib "user32" (ByVal hWndChild As Long, ByVal hWndNewParent As Long) As Long
```


### Source Code

```
Dim SysListView As Long
Dim SHELLDLLDefView As Long
Dim Progman As Long
Progman = FindWindow("Progman", vbNullString)
SHELLDLLDefView = FindWindowEx(Progman, 0, "SHELLDLL_DefView", vbNullString)
SysListView = FindWindowEx(SHELLDLLDefView, 0, "SysListView32", vbNullString)
Call SetParent(SysListView, Me.hWnd)
```

