# Changelog — yd-enterprise-info

## v26.4.29.1545 (2026-04-29，当前版本)

- 初始发布版本，基于元典开放平台 `https://open.chineselaw.com`
- 封装全部 22 个企业信息接口，支持分页自动翻取
- 鉴权通过环境变量 `CHINESELAW_API_KEY` 或 `--api-key` 参数传入
- 分页接口默认 `--max-pages 20` 防止积分超耗；`--yes` 跳过逐次确认提示
- 落盘格式：`<subcommand>_<identifier>_<YYYYMMDDHHMM>.json`，根节点追加 `_meta` 字段（fetched_pages / total / fetched_at）
- 零第三方依赖，仅使用 Python 标准库

### 覆盖子命令（22 个）

`search-company` · `base-info` · `change` · `brand` · `soft-right` · `patent` · `copyright-work` · `website` · `outbound-invest` · `outbound-guarantee` · `equity-pledge` · `equity-frozen` · `abnormal` · `serious-violation` · `tax-arrears` · `admin-penalty` · `executed` · `dishonest` · `litigation-doc` · `litigation-stat` · `court-announcement` · `court-hearing`
