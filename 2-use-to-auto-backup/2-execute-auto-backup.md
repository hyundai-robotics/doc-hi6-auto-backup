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