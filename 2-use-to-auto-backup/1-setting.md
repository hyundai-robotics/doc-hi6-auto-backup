# 2.1 Settings

Navigate to `[F2: System] – 2: Control parameter – 8: Automatic Backup & Restoration`.

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
</table>