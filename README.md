<p align="center"><img src="docs/images/logo.png" width="160" alt="Season Marker"></p>

# Season Marker

Emby 的 STRM 片头标记插件。主要用来解决 Emby 不会主动分析 STRM 片头的问题，也可以在管理页手动修改某一集的片头、片尾时间。

![插件页面](docs/images/plugin-card.png)

![媒体管理页面](docs/images/management.png)

> 截图中的剧名和时间为演示数据。

## 支持的功能

- 分析 STRM 剧集片头
- 按媒体库、电视剧、季、集浏览
- 手动修改单集片头结束和片尾开始时间
- 重新分析本季或单集
- 新增剧集后增量分析
- Emby 计划任务

自动分析只处理片头，片尾仍然需要手动设置。

## 安装

1. 下载 [SeasonMarker.dll](https://github.com/xpg8802667/SeasonMarker/releases/latest/download/SeasonMarker.dll)。
2. 复制到 Emby 配置目录：

   ```text
   /config/plugins/SeasonMarker.dll
   ```

3. 重启 Emby。
4. 在“控制台 → 插件”中打开 `Season Marker`。

升级时直接替换 DLL，然后重启 Emby 即可。

## 使用

### 查看和修改标记

进入“媒体浏览”，依次选择媒体库、电视剧、季和剧集。点击单集后，可以查看并修改：

- 片头结束时间
- 片尾开始时间

片头开始固定为 `00:00:00`。单集手动保存后不会被普通自动分析覆盖。

### 分析片头

- 在季度页面点击“重新分析本季”。
- 在单集编辑页面点击“重新分析本集”。
- 在“自动分析”中开启新增剧集分析，适合仍在更新的连载剧。
- 也可以在“控制台 → 计划任务”中手动运行或设置定时任务。

## 使用前注意

- 目前只测试了 Emby `4.9.5.x` 版本，其他版本请自行测试。
- Emby 原生片头功能需要 Premiere。