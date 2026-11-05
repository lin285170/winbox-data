# winbox-data

Winbox 站点抓取产物，**只读公开仓库**，供客户端通过 jsdelivr / raw 读取。

## 目录

```
data/
  index.json            站点索引与统计
  {sid}.json            单个站点全量数据
  {sid}/{cat}.json      分类分片（前端按分类加载的就是这个）
  {sid}/_index.json     轻量搜索索引
```

`sid` 目前有 `hjzhencai`（花卷影视）、`libvio`（LIBVIO）、`ddys`（低端影视）。

## 消费方式

```
https://cdn.jsdelivr.net/gh/lin285170/winbox-data@main/data/{sid}/{cat}.json
https://raw.githubusercontent.com/lin285170/winbox-data/main/data/{sid}/{cat}.json
```

jsdelivr 单文件上限 20MB，超限的文件（如 `ddys.json`）会 404，需回落到 raw。

## 说明

本仓库由抓取流程自动生成，内容为站点公开的影片元数据与分享链接索引，
不含任何账号凭据。请勿手动修改 `data/` 下的文件。
