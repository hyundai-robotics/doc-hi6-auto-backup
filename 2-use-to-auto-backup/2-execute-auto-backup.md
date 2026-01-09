# 2.2 Execution of Automatic Backup

A backup is executed at the moment the configured backup conditions are met.
Backups are performed in any situation, including during the settings screen, teaching operations, jogging, or robot playback in Automatic mode.
However, a backup will not be executed while another backup or a restore operation is already in progress.

During the backup process, a message box like the one shown below appears on the screen.
Please stop all operations and wait until the completion message is displayed.


![](../_assets/backup_st.png)

![](../_assets/backup_doing.png)

![](../_assets/backup_en.png)

The backup data are stored in the following paths on the Teach Pendant or the main module.

<style type="text/css">
table  {border-collapse:collapse;}
td {border-color:gray;border-style:solid;border-width:1px;}
.grayed {background-color:lightgray; color:black}
</style>

<table>
	<tr>
		<td class='grayed'>
			<p>Path Name - TP</p>
		</td>
		<td>
			<p>/usr/share/hyundai/hi6/backup/ts/</p>
		</td>
		<td>
			<p>`backup/ts/` under the TP item in the File Manager screen</p>
		</td>
	</tr>
	<tr>
		<td class='grayed'>
			<p>Path Name - MAIN</p>
		</td>
		<td>
			<p>/ata0:2/lib/hi6/backup/ts/</p>
		</td>
		<td>
			<p>`backup/ts/` under the MAIN item in the File Manager screen</p>
		</td>
	</tr>
	<tr>
		<td class='grayed'>
			<p>Generated Subfolder Name</p>
		</td>
		<td>
			<p>Format: b{date}_{time}</p>
		</td>
		<td>
			<p>The prefix "b" indicates backup</p>
		</td>
	</tr>
</table>

Example:<br>
MAIN/backup/ts/b20230512_1730/

If the available free space on the main board is less than 10%, the oldest backup point is deleted before performing a new backup.
If insufficient free space is detected during the backup process, the backup operation is aborted.

By opening the History window, you can view records of backup start, completion, and errors

If you enable the `Notification (+N)` filter in the `history` window, you can view the records of backup start and completion.

![](../_assets/backup_log.png)
