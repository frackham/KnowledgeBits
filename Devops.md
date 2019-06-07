## DevOps

### Release management
@mipsytipsy thread reader unroll thread on release engineering: "every company I know of with >40 eng is systematically underinvesting in release engineering..."




## TFS / VSTS Integration
https://spin.atomicobject.com/2018/11/28/nodejs-excel-file-generation/
Could insert a background sheet for TFS to work with?
TFS
https://stackoverflow.com/questions/40143373/procedure-to-write-and-execute-custom-queries-for-visual-studio-team-servicesvs
These are then executable!! “selecting File, Save Query As” (Assume same for Azure devops?).
http://www.woodwardweb.com/vsts/tfs_top_tip_1_w.html
http://amolpandey.com/2018/08/26/vsts-tfs-online-create-work-item-from-outlook-mail-integration-via-vsto/
https://mohamedradwan.com/2018/04/12/migrating-tfs-and-vsts-work-items-using-vsts-work-item-migrator/
https://stackoverflow.com/questions/17868281/how-to-find-work-item-that-are-assigned-by-me <-- not at the moment, but at some point
https://xebia.com/blog/how-to-deal-with-the-current-sprintiteration-in-tfs-queries/
### WIQL
Form Visual Studio query in Team Explorer, save as WIQL. These are then executable!!



## CLI/ DEvops
https://stackoverflow.com/questions/368041/how-to-code-a-spinner-for-waiting-processes-in-a-batch-file
Node equivalent: https://github.com/bitifet/smart-spinner
@devopsdotcom: Scripts in the Development Pipeline: Best Practices for Avoiding the ‘Scriptocalypse’ https://devops.com/scripts-in-the-development-pipeline-best-practices-for-avoiding-the-scriptocalypse/
Future PRs
Things to help work:
-           https://github.com/Microsoft/vscode-htmlhint/issues/33 <-- also, ideally htmlhint should support ignore files… see other projects.

## Git
Git cheat sheet - https://github.com/bennadel/git-cheat-sheet

Meet GitHub Actions 👋
It might just change the way you work.
http://github.com/features/actions https://twitter.com/github/status/1052248654445076481/video/1
https://cmatskas.com/how-to-update-your-git-credentials-on-windows/
git log ae7a0e86..feature/69575_69585_69587_AdminUI –oneline
git log ae7a0e86..feature/69575_69585_69587_AdminUI –oneline
specific commit of a different branch
feature branch
Tried and works in VS code terminal – shows summary of commit messages between the 2.
git diff ae7a0e86..feature/69575_69585_69587_AdminUI --compact-summary
git diff ae7a0e86..feature/69575_69585_69587_AdminUI --compact-summary
specific commit of a different branch
feature branch
For files:
--compact-summary
remove cached git folder so gitignore picks it up
git rm -r --cached myFolder
git  avoid assume unchanged for (e.g.) gitignore
You want skip-worktree.    [   git update-index --skip-worktree <file_name>   ]
assume-unchanged is designed for cases where it is expensive to check whether a group of files have been modified; when you set the bit, git (of course) assumes the files corresponding to that portion of the index have not been modified in the working copy. So it avoids a mess of stat calls. This bit is lost whenever the file's entry in the index changes (so, when the file is changed upstream).
skip-worktree is more than that: even where git knows that the file has been modified (or needs to be modified by a reset --hard or the like), it will pretend it has not been, using the version from the index instead. This persists until the index is discarded.
There is a good summary of the ramifications of this difference and the typical use cases here: http://fallengamer.livejournal.com/93321.html .
From that article:
•           --assume-unchanged assumes that a developer shouldn’t change a file. This flag is meant for improving performance for not-changing folders like SDKs.
•           --skip-worktree is useful when you instruct git not to touch a specific file ever because developers should change it. For example, if the main repository upstream hosts some production-ready configuration files and you don’t want to accidentally commit changes to those files, --skip-worktree is exactly what you want.


## Powershell
MAIL:
# $Outlook = New-Object -ComObject Outlook.Application
# $Mail = $Outlook.CreateItem(0)
# $Mail.To = "Fraser.Rackham@peninsula-uk.com"
# $Mail.Subject = "Action"
# $Mail.Body ="Test"
# $Mail.Send()
Function Global:Send-Email {
[cmdletbinding()]
Param (
[Parameter(Mandatory=$False,Position=0)]
[String]$Address = "Fraser.Rackham@peninsula-uk.com",
[Parameter(Mandatory=$False,Position=1)]
[String]$Subject = "Default Email subject",
[Parameter(Mandatory=$False,Position=2)]
[String]$Body = "Default mail body"
      )
Begin {
Clear-Host
# Add-Type -assembly "Microsoft.Office.Interop.Outlook"
    }
Process {
# Create an instance Microsoft Outlook
$Outlook = New-Object -ComObject Outlook.Application
$Mail = $Outlook.CreateItem(0)
$Mail.To = "$Address"
$Mail.Subject = $Subject
$Mail.Body =$Body
# $Mail.HTMLBody = "When is swimming?"
# $File = "D:\CP\timetable.pdf"
# $Mail.Attachments.Add($File)
$Mail.Send()
       } # End of Process section
End {
# Section to prevent error message in Outlook
# $Outlook.GetNameSpace("MAPI").SendAndReceive(1)
$Outlook.Quit()
[System.Runtime.Interopservices.Marshal]::ReleaseComObject($Outlook)
$Outlook = $null
   } # End of End section!
} # End of function
# Example of using this function
Send-Email #-Address deck@swimmingpool.com
# Research properties for your email
Clear-Host
Add-Type -Assembly "Microsoft.Office.Interop.Outlook"
$Outlook = New-Object -ComObject Outlook.Application
$Mail = $Outlook.CreateItem(0)
$Mail | Get-Member -MemberType Properties #List properties of mail object
$Outlook | Get-Member -MemberType Method #List methods of outlook.
Basics / setup in addition:
Execution policy issue?: (see: https://blog.netspi.com/15-ways-to-bypass-the-powershell-execution-policy/ )
1.         From within a batch:
PowerShell.exe -ExecutionPolicy Bypass -File untitled1.ps1
2.         Setting at command line (on login?)
Set-ExecutionPolicy -ExecutionPolicy Bypass
Current working directory:                           i.e.       %~dp0
$PSScriptRoot
(not in early versions).
Print line
Write-Host: Write directly to the console, not included in function/cmdlet output. Allows foreground and background colour to be set.
Write-Debug: Write directly to the console, if $DebugPreference set to Continue or Stop.
Write-Verbose: Write directly to the console, if $VerbosePreference set to Continue or Stop.
