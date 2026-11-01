# 来源与修改声明 / Provenance and modifications

本仓库是**个人自用的构建/发布镜像**，不是上游官方产物，与上游作者无隶属或背书关系。

## 上游

- `LIghtJUNction/MagicNet` — <https://github.com/LIghtJUNction/MagicNet>，MIT，© 2025 LIghtJUNction

## 本仓库的修改

- 发布工作流改用 Rust 安装器 helper（`magicnet-components`），不再打包 Go helper；
- 子模块固定到本账号镜像，`checkout` 与构建来源元数据改为随仓库属主解析；
- 发布包中的核心由模块仓的 `android/arm64` 构建路径产出（Rust2 扫描、无 lxd、惰性路径）。

## 许可

沿用上游 **MIT**（见 `LICENSE`）；子模块各自适用其许可，其中 `sing-box` 为 **GPL-3.0**。

## 免责

仅供个人使用，不提供任何担保；使用风险自负。
本仓库不包含订阅、节点凭据、个人配置或设备数据。
