
[__SOURCE](README.md)
# ${cont_model} 机器人控制器功能手册 - 自动备份

{% endhint %}
[__SOURCE](0-about-this-manual/README.md)
# 关于手册
[__SOURCE](0-about-this-manual/precautions.md)
# 注意事项

{% include file="zh/precautions.md" %}
[__SOURCE](0-about-this-manual/safety-notice.md)
# 安全注意事项

{% include file="zh/safety-notice.md" %}
[__SOURCE](1-overview/README.md)
# 1. 概述
[__SOURCE](1-overview/1-prerequisite.md)
# 1.1 前提条件

理解本手册所需的知识。

* [${cont_model} 机器人控制器操作手册](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/ko-tp630/README?cont_model=${cont_model})
[__SOURCE](1-overview/2-about-auto-backup.md)
# 1.2 关于自动备份功能

自动备份功能根据预定义条件自动或手动备份当前 `project/` 文件夹和整个 ` (log/)` 文件夹的 ${cont_model} 控制器。
用户可以通过选择其中一个保存的备份点来恢复系统。
当 ${cont_model} 控制器的文件因故障或用户错误而被删除或损坏时，这些备份数据将被使用。

备份操作可以使用以下三种方法配置：

1. 在指定的星期几和时间（最多可以设置四个日程）

2. 当指定的输入分配信号被开启时

3. 当操作模式从手动切换到自动时
[__SOURCE](2-use-to-auto-backup/README.md)
# 2. 使用自动备份
[__SOURCE](2-use-to-auto-backup/1-setting.md)
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
[__SOURCE](2-use-to-auto-backup/2-execute-auto-backup.md)
# 2.2 自动备份的执行

当满足配置的备份条件时，备份将被执行。
无论在设置屏幕、教学操作、走动或机器人在自动模式下播放时，都会执行备份。
但是，在另一个备份或恢复操作正在进行时，不会执行备份。

在备份过程中，屏幕上会出现如下面所示的消息框。
请停止所有操作，并等待直到出现完成消息。


![](../_assets/backup_st.png)

![](../_assets/backup_doing.png)

![](../_assets/backup_en.png)

备份数据存储在教学挂件或主模块的以下路径中。

<style type="text/css">
table  {border-collapse:collapse;}
td {border-color:gray;border-style:solid;border-width:1px;}
.grayed {background-color:lightgray; color:black}
</style>

<table>
	<tr>
		<td class='grayed'>
			<p>路径名称 - TP</p>
		</td>
		<td>
			<p>/usr/share/hyundai/hi6/backup/ts/</p>
		</td>
		<td>
			<p>`backup/ts/` 在文件管理器屏幕中的 TP 项下</p>
		</td>
	</tr>
	<tr>
		<td class='grayed'>
			<p>路径名称 - MAIN</p>
		</td>
		<td>
			<p>/ata0:2/lib/hi6/backup/ts/</p>
		</td>
		<td>
			<p>`backup/ts/` 在文件管理器屏幕中的 MAIN 项下</p>
		</td>
	</tr>
	<tr>
		<td class='grayed'>
			<p>生成的子文件夹名称</p>
		</td>
		<td>
			<p>格式: b{date}_{time}</p>
		</td>
		<td>
			<p>前缀 "b" 表示备份</p>
		</td>
	</tr>
</table>

示例:<br>
MAIN/backup/ts/b20230512_1730/

如果主板上的可用空闲空间少于 10%，则在执行新的备份前将删除最旧的备份点。
如果在备份过程中检测到可用空间不足，则备份操作将被中止。

通过打开历史窗口，您可以查看备份开始、完成和错误的记录。

如果在`运行履历 (history)`窗口中启用`通知 (+N)`过滤器，您可以查看备份开始和完成的记录。

![](../_assets/backup_log.png)
[__SOURCE](2-use-to-auto-backup/3-restoration.md)
# 2.3 恢复

Navigate to `[F2: 系统] - 2: 控制参数 - 8: Automatic backup & restoration ([F2: system] - 2: Control parameter - 8: Automatic backup & restoration)`.

Click the [F1: Restore] button to display the screen shown below.

![Fig. restore dialog-box](../_assets/restore.png)

The list box displays available restore points sorted by the time they were backed up.
The item at the bottom of the list is the most recent backup point.

* `[Delete]`: Select the items to delete and press this button. After user confirmation, the selected folders are deleted.

* `[Restore]`: Select the item to restore and press this button. After user confirmation, the restore process begins.

When the restore process is completed, a message like the one shown below is displayed.
After re-power the system, the system will be ready for normal operation.

![Fig. restoration completed](<../_assets/restored_reboot.png>)
[__SOURCE](appendices/rules-occupational-safety.md)
# 职业安全与健康标准规则以及安全检查通知

工业机器人应根据《职业安全与健康标准规则》和《安全检查通知》的检查标准进行安装（如果需接受检查）。

"[职业安全与健康标准规则](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/zh/README)"
[__SOURCE](quality-assurance.md)
# 质量保证

"[Quality Assurance](https://hrbook-hrc.web.app/#/view/quality-assurance/zh/README)"