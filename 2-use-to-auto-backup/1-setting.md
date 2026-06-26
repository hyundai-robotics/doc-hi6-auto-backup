# 2.1 设置

Navigate to `[F2: 系统] - 2: 控制参数 - 8: Automatic Backup & Restoration ([F2: System] - 2: Control parameter - 8: Automatic Backup & Restoration)`.

Press the `[F2: Backup Now]` button to perform a backup immediately, regardless of the current settings.
(Only the `automatic backup storage location` follows the currently saved configuration.)

After configuring the items on the screen, press the `[F7: 确定] ([F7: OK])` button to save and apply the settings.
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
			条目
		</th>
		<th colspan="2">
			描述
		</th>
		<th>
			备注
		</th>
	</tr>
</thead>	
<tbody>
	<tr>
		<td>
			自动备份存储
		</td>
		<td colspan="2">
			TP: 指定是否备份到教导挂件存储设备。<br>
			MAIN: 指定是否备份到主模块 (COM) 存储。
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			最大备份版本数
		</td>
		<td colspan="2">
			设置要保留的最大备份点数量。
			当备份数量超过指定限制时，最旧的备份文件夹会被自动删除。
		</td>
		<td>
			1~100
		</td>
	</tr>
	<tr>
		<td>
			自由空间：
		</td>
		<td colspan="2">
			配置自动备份在选定星期几的每天或特定时间执行。
			最多可以设置四个时间表。通过取消选中不使用的时间表来禁用它们。
		</td>
		<td>
			00:00
			~
			23:59
		</td>
	</tr>
	<tr>
		<td rowspan="4">
			模式更改时备份<br>
			(手动 -> 自动)
		</td>
		<td colspan="2">
			配置在模式从手动更改为自动时是否执行备份。
		</td>
		<td rowspan="4">
			-
		</td>
	</tr>
	<tr>
		<td>
			- 禁用：
		</td>
		<td>
			不执行备份。
		</td>
	</tr>
	<tr>
		<td>
			- 用户确认：
		</td>
		<td>
			显示对话框询问用户是否执行备份。如果用户选择“是”，则执行备份。
		</td>
	</tr>
	<tr>
		<td>
			- 无确认：
		</td>
		<td>
			立即执行备份，而不显示确认对话框。
		</td>
	</tr>
	<tr>
		<td>
			输入分配信号<br>
			(运行备份)
		</td>
		<td colspan="2">
			在指定输入信号打开时执行备份。
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			输出分配信号<br>
			(备份期间)
		</td>
		<td colspan="2">
			在备份进行时，指定的输出信号打开。
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			输出分配信号<br>
			(备份错误)
		</td>
		<td colspan="2">
			在备份过程中发生错误时打开。
			通过按两次 [Reset] 键或按 [Reset][0][ENTER] 来清除信号。
		</td>
		<td>
			-
		</td>
	</tr>
<tbody>
</table>


Assignment Signal Settings 示例。

<table>
<thead>
	<tr>
		<th>
			信号类型
		</th>
		<th>
			设置示例
		</th>
		<th>
			结果
		</th>
	</tr>
</thead>
<tbody>
	<tr>
		<td>
			fb0. 省略标记
		</td>
		<td>
			135
		</td>
		<td>
			135 (do135 或 di135)
		</td>
	</tr>
	<tr>
		<td>
			fb. 对象标记
		</td>
		<td>
			5.220
		</td>
		<td>
			fb5.220 (do220 或 di220 of fb5)
		</td>
	</tr>
	<tr>
		<td>
			fn. 对象标记
		</td>
		<td>
			.13.94
		</td>
		<td>
			fn13.94 (fb的特定区域的 do94，或 di94)
		</td>
	</tr>
</tbody>
</table>