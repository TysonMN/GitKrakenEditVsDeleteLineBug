Steps to reproduce:

1.	Clone this GitHub repository
2.	Checkout the branch called `branch`
3.	Under “LOCAL”, right-click the branch called `main`
4.	Select “Rebase branch onto main”
5.	Select the conflicted file
6.	Observe the diff `B` on right side and the final diff below both before and after selecting all the changes from `B`.

Expected behavior:
Diff `B` and the final diff show line 2 containing `Line2` as deleted and the line containing `Line3` as being on line 2.

Actual behavior:
Diff `B` and the final diff show line 2 containing `Line2` as replaced by an empty line and the line containing `Line3` as being on line 3.  However, when looking at the diff after the rebase is complete, the expected behavior is observed.

Here is a screenshot after step 5.
<img src="https://raw.githubusercontent.com/TysonMN/GitKrakenEditVsDeleteLineBug/main/1_GitKraken_merge_start.png"/>

Here is a screenshot after step 5 and after selecting `B`.
<img src="https://raw.githubusercontent.com/TysonMN/GitKrakenEditVsDeleteLineBug/main/2_GitKraken_merge_resolved.png"/>

Here is a screenshot after the merege is complete.  It shows the correct line numbers in the diff.
<img src="https://raw.githubusercontent.com/TysonMN/GitKrakenEditVsDeleteLineBug/main/3_GitKraken_resulting_commit_diff.png"/>

Also, for what it is worth, here is the file contents displayed by Visual Studio Code after the merge is complete.
<img src="https://raw.githubusercontent.com/TysonMN/GitKrakenEditVsDeleteLineBug/main/4_merged_file.png"/>
