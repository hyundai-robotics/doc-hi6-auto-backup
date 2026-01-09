# Hi6 Robot Controller Function Manual - Auto Backup

{% endhint %}
# 1. Overview

# 1.1 Prerequisite

The following knowledge is necessary to understand this manual.

* [Hi6 Robot Controller Operation Manual](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-Hi6-tp630/README)
# 1.2 About the Auto Backup Function

The Auto Backup function automatically or manually backs up the current `project/` folder and the entire `log/` folder of the Hi6 controller according to predefined conditions.
Users can restore the system by selecting one of the saved backup points.
These backup data are used when files of the Hi6 controller are deleted or damaged due to a malfunction or user error.

The backup operation can be configured using the following three methods:

1. At specified days of the week and times (up to four schedules can be set)

2. When a specified input assignment signal is turned ON

3. When the operating mode is switched from Manual to Automatic
# 2. Using the Auto Backup

# 2.1 Settings

Navigate to `[F2: System] - 2: Control parameter - 8: Automatic Backup & Restoration`.

Press the `[F2: Backup Now]` button to perform a backup immediately, regardless of the current settings.
(Only the `automatic backup storage location` follows the currently saved configuration.)

After configuring the items on the screen, press the `[F7: OK]` button to save and apply the settings.
The meanings of each item are described in the table below.

<style type="text/css">
table  {border-collapse:collapse;}
td {border-color:gray;border-style:solid;border-width:1px;}
.grayed {background-color:lightgray; color:black}
</style>

<table class="tg">
<thead>
	<tr>
		<th>
			Entry
		</th>
		<th colspan="2">
			Description
		</th>
		<th>
			Notes
		</th>
	</tr>
</thead>	
<tbody>
	<tr>
		<td>
			Automatic-backup storage
		</td>
		<td colspan="2">
			TP: Specifies whether to back up to the Teach Pendant storage device.<br>
			MAIN: Specifies whether to back up to the main module (COM) storage.
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			Maximum number of backup versions
		</td>
		<td colspan="2">
			Sets the maximum number of backup points to retain.
			When the number of backups exceeds the specified limit, the oldest backup folders are automatically deleted.
		</td>
		<td>
			1~100
		</td>
	</tr>
	<tr>
		<td>
			Free space:
		</td>
		<td colspan="2">
			Configures automatic backups to be performed daily or at a specific time on selected days of the week.
			Up to four schedules can be set. Disable unused schedules by unchecking them.
		</td>
		<td>
			00:00
			~
			23:59
		</td>
	</tr>
	<tr>
		<td rowspan="4">
			Backup on mode change<br>
			(Manual -> Auto)
		</td>
		<td colspan="2">
			Configures whether a backup is performed at the moment the mode changes from Manual to Automatic.
		</td>
		<td rowspan="4">
			-
		</td>
	</tr>
	<tr>
		<td>
			- Disable:
		</td>
		<td>
			No backup is performed.
		</td>
	</tr>
	<tr>
		<td>
			- User confirm:
		</td>
		<td>
			Displays a dialog asking the user whether to perform a backup. Backup is executed if the user selects 'Yes'.
		</td>
	</tr>
	<tr>
		<td>
			- No confirm:
		</td>
		<td>
			Performs a backup immediately without displaying a confirmation dialog.
		</td>
	</tr>
	<tr>
		<td>
			Input assignment signal<br>
			(run backup)
		</td>
		<td colspan="2">
			Executes a backup at the moment the specified input signal turns ON.
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			Output assignment signal<br>
			(during backup)
		</td>
		<td colspan="2">
			The specified output signal turns ON while a backup is in progress.
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			Output assignment signal<br>
			(backup error)
		</td>
		<td colspan="2">
			Turns ON when an error occurs during the backup process.
			The signal is cleared by pressing the [Reset] key twice, or by pressing [Reset][0][ENTER].
		</td>
		<td>
			-
		</td>
	</tr>
<tbody>
</table>


Example of Assignment Signal Settings.

<table>
<thead>
	<tr>
		<th>
			Signal Type
		</th>
		<th>
			Setting Example
		</th>
		<th>
			Result
		</th>
	</tr>
</thead>
<tbody>
	<tr>
		<td>
			fb0. omitted notation
		</td>
		<td>
			135
		</td>
		<td>
			135 (do135 or di135)
		</td>
	</tr>
	<tr>
		<td>
			fb. object notation
		</td>
		<td>
			5.220
		</td>
		<td>
			fb5.220 (do220 or di220 of fb5)
		</td>
	</tr>
	<tr>
		<td>
			fn. object notation
		</td>
		<td>
			.13.94
		</td>
		<td>
			fn13.94 (fb's specific region's do94, or di94)
		</td>
	</tr>
</tbody>
</table># 2.2 Execution of Automatic Backup

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
# 2.3 Restore

Navigate to `[F2: system] - 2: Control parameter - 8: Automatic backup & restoration`.

Click the [F1: Restore] button to display the screen shown below.

![Fig. restore dialog-box](../_assets/restore.png)

The list box displays available restore points sorted by the time they were backed up.
The item at the bottom of the list is the most recent backup point.

* `[Delete]`: Select the items to delete and press this button. After user confirmation, the selected folders are deleted.

* `[Restore]`: Select the item to restore and press this button. After user confirmation, the restore process begins.

When the restore process is completed, a message like the one shown below is displayed.
After re-power the system, the system will be ready for normal operation.

![Fig. restoration completed](<../_assets/restored_reboot.png>)
# Rules on Occupational Safety and Health Standards, and Notice for Safety Inspection

The industrial robot should be installed in consideration of the inspection standards both of the Rules on Occupational Safety and Health Standards and of the Notice for Safety Inspection \(if subject to inspection\).

"[Rules on Occupational Safety and Health Standards](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/english/README)"
# Quality Assurance

"[Quality Assurance](https://hrbook-hrc.web.app/#/view/quality-assurance/english/README)"
