# 2.1 设置

导航到 `[F2: 系统] - 2: 控制参数 - 8: 自动备份与恢复 ([F2: System] - 2: Control parameter - 8: Automatic Backup & Restoration)`。

按 `[F2: 立即备份]` 按钮立即执行备份，无论当前设置如何。
（仅 `自动备份存储位置` 会遵循当前保存的配置。）

在配置屏幕上的项目后，按 `[F7: 确认] ([F7: OK])` 按钮保存并应用设置。
每个项目的含义在下面的表格中描述。

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
			TP: 指定是否备份到教学 pendant 存储设备。<br>
			MAIN: 指定是否备份到主模块 (COM) 存储。
		</td>
		<td>
			-
		</td>
	</tr>
	<tr>
		<td>
			最大备份版本数量
		</td>
		<td colspan="2">
			设置保留的最大备份点数。
			当备份数量超过指定限制时，最旧的备份文件夹会被自动删除。
		</td>
		<td>
			1~100
		</td>
	</tr>
	<tr>
		<td>
			可用空间：
		</td>
		<td colspan="2">
			配置每日或特定时间在一周的选定天进行自动备份。
			最多可以设置四个时间表。通过取消选中来禁用未使用的时间表。
		</td>
		<td>
			00:00
			~
			23:59
		</td>
	</tr>
	<tr>
		<td rowspan="4">
			模式切换时备份<br>
			(手动 -> 自动)
		</td>
		<td colspan="2">
			配置在模式从手动切换到自动的瞬间是否执行备份。
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
			- 无需确认：
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
			当指定的输入信号打开时，执行备份。
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
			在备份进行时，指定的输出信号会打开。
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
			使用[重置]键按两次或按[重置][0][ENTER]来清除信号。
		</td>
		<td>
			-
		</td>
	</tr>
<tbody>
</table>


分配信号设置示例。

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
			fb0.省略符号
		</td>
		<td>
			135
		</td>
		<td>
			135 (do135或di135)
		</td>
	</tr>
	<tr>
		<td>
			fb.对象符号
		</td>
		<td>
			5.220
		</td>
		<td>
			fb5.220 (do220或di220 of fb5)
		</td>
	</tr>
	<tr>
		<td>
			fn.对象符号
		</td>
		<td>
			.13.94
		</td>
		<td>
			fn13.94 (fb的特定区域的do94，或di94)
		</td>
	</tr>
</tbody>
</table>