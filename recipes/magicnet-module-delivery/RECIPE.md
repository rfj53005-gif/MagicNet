# MagicNet 模块安装、组件分发与安全更新

~~~toml
format = "recipkg/1"

[package]
name = "magicnet-module-delivery"
version = "0.2.2"
kind = "software"
description = "MagicNet 模块安装、组件分发与安全更新"
entry = "BUILD_PROMPT.md"
~~~

配方版本与被观察软件版本分开管理；来源为 MagicNet v1.7.2，提交 96993ea5c851b8d51cc562c3ca0766a2ca571210。实现源码不属于本包。

0.2.2 记录组件引导安装器完成 Rust 移植并进入发布链：`bin/magicnet-components` 由 `crates/magicnet-components`（共享 `crates/magicnet-installer` 库）以 aarch64-linux-android musl 静态构建（约 600 KB，替换 Go 版 2-3 MB），命令面、`[error]` 前缀与退出码与 Go 实现保持等价（54/54 等价测试、test-components 17/17、test-installer-identity 通过，含真机 usage 冒烟）。源码提交 magicnet-android@01aa82b9（其 sing-box gitlink 为 integration/rust2-p3-on-ff669d45@27834fbd：Rust2 流式扫描 + Android 线裁剪 lxd 守护进程，-310 KB；fdtrack 经整核 A/B 判定不合入）。本次为本地整合，尚未推送公开仓库。

2026-10-29 本轮读取固定 v1.8.0 源码 0dca28dd984d82333707cbf4b222596934b4d847 并补齐重建合同；来源与实际验证见根 SOURCE_AUDIT.md、PROVENANCE.md、VERIFICATION.md。本次配方升级不表示 Android 实现已修复或已发布。
