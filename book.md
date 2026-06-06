
[__SOURCE](README.md)
# ${cont_model} 机器人控制器功能手册 - 自动备份

{% endhint %}
[__SOURCE](0-about-this-manual/README.md)
# 关于手册

在使用产品之前，您必须充分理解手册的内容。此外，请将手册放在身边，以便随时参考。

本手册可作为已购买HD Hyundai Robotics产品客户的参考材料，或可用作内部培训材料。

本手册是基于标准规格编写的，因此某些内容可能因您购买的产品型号而有所不同。此外，为了改善产品性能，本手册的内容和规格可能会随时更改，HD Hyundai Robotics对因手册中的不准确或错字而可能导致的情况不承担责任。有关手册修订的详细信息，您需要访问我们的互联网网站 [http://www.hyundai-robotics.cn/](http://www.hyundai-robotics.cn/)。

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

理解本手册需要以下知识。

* [${cont_model} 机器人控制器操作手册](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/ko-tp630/README?cont_model=${cont_model})
[__SOURCE](1-overview/2-about-auto-backup.md)
# 1.2 关于自动备份功能

自动备份功能根据预定义条件自动或手动备份当前 `project/` 文件夹和整个 `日志/ (log/)` 文件夹的 ${cont_model} 控制器。
用户可以通过选择已保存的备份点来恢复系统。
当 ${cont_model} 控制器的文件因故障或用户错误被删除或损坏时，这些备份数据会被使用。

备份操作可以使用以下三种方法进行配置：

1. 在指定的星期几和时间（最多可以设置四个计划）

2. 当指定的输入指派信号被打开时

3. 当操作模式从手动切换到自动时
[__SOURCE](2-use-to-auto-backup/README.md)
# 2. 使用自动备份
[__SOURCE](2-use-to-auto-backup/1-setting.md)
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
[__SOURCE](2-use-to-auto-backup/2-execute-auto-backup.md)
# 2.2 自动备份的执行

当满足配置的备份条件时，会执行备份。
备份在任何情况下进行，包括在设置屏幕、教学操作、慢走或机器人在自动模式下播放时。
但是，当另一个备份或还原操作正在进行时，不会执行备份。

在备份过程中，屏幕上会出现如下所示的消息框。
请停止所有操作，并等待完成消息显示。

![](../_assets/backup_st.png)

![](../_assets/backup_doing.png)

![](../_assets/backup_en.png)

备份数据存储在教导吊舱或主模块的以下路径中。

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
			<p>`backup/ts/` 在文件管理器屏幕的TP项目下</p>
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
			<p>`backup/ts/` 在文件管理器屏幕的MAIN项目下</p>
		</td>
	</tr>
	<tr>
		<td class='grayed'>
			<p>生成的子文件夹名称</p>
		</td>
		<td>
			<p>格式：b{date}_{time}</p>
		</td>
		<td>
			<p>前缀“b”表示备份</p>
		</td>
	</tr>
</table>

示例：<br>
MAIN/backup/ts/b20230512_1730/

如果主板上的可用空闲空间少于10%，则在执行新备份之前，会删除最旧的备份点。
如果在备份过程中检测到空闲空间不足，则备份操作将被中止。

通过打开历史窗口，您可以查看备份开始、完成和错误的记录。

如果您在“历史 (history)”窗口中启用“通知 (+N)”过滤器，则可以查看备份开始和完成的记录。

![](../_assets/backup_log.png)
[__SOURCE](2-use-to-auto-backup/3-restoration.md)
# 2.3 恢复

导航到 `[F2: 系统] - 2: 控制参数 - 8: 自动备份与恢复 ([F2: system] - 2: Control parameter - 8: Automatic backup & restoration)`。

点击 [F1: 恢复] 按钮以显示如下所示屏幕。

![Fig. restore dialog-box](../_assets/restore.png)

列表框显示按备份时间排序的可用恢复点。
列表底部的项目是最新的备份点。

* `[删除]`: 选择要删除的项目并按此按钮。在用户确认后，所选文件夹将被删除。

* `[恢复]`: 选择要恢复的项目并按此按钮。在用户确认后，恢复过程开始。

当恢复过程完成时，将显示如下所示的消息。
重新启动系统后，系统将准备好正常操作。

![Fig. restoration completed](<../_assets/restored_reboot.png>)
[__SOURCE](appendices/rules-occupational-safety.md)
# 职业安全与健康标准的规则，以及安全检查通知

工业机器人应考虑到职业安全与健康标准的规则和安全检查通知的检查标准进行安装（如果需要检查）。

"[职业安全与健康标准的规则](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/en/README)"
[__SOURCE](quality-assurance.md)
# 质量保证

"[Quality Assurance](https://hrbook-hrc.web.app/#/view/quality-assurance/en/README)"