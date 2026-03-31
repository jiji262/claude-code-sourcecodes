# Claude Code Sourcecodes

基于 Claude Code 公开分发产物整理的独立研究镜像。

[English](./README.md) | [简体中文](./README.zh-CN.md)

> [!IMPORTANT]
> 本仓库为非官方整理版本，与 Anthropic 不存在隶属、背书、维护或授权关系。
>
> 仓库内容主要基于公开分发的 [`@anthropic-ai/claude-code`](https://www.npmjs.com/package/@anthropic-ai/claude-code) `2.1.88` npm 包、包内附带的 `cli.js.map` source map，以及围绕这些公开产物的公开社区讨论整理而成。
>
> 整理过程中未使用任何私有仓库访问权限、泄露凭证或其他非公开源码材料。

> [!CAUTION]
> 相关版权、商标及其他权利仍归其各自权利人所有。
>
> 本仓库仅面向研究、互操作性分析、教学和归档参考，不应被视为官方上游仓库，也不构成任何“在所有法域都可自由再分发”的法律意见。
>
> 在使用、复制、再分发或基于这些材料继续开发前，请自行评估所在地区法律、适用许可条款及内部合规要求。

## 这是什么

本仓库是对公开发布版 Claude Code 包内容所做的研究型重建，目的是帮助读者查看公开包是如何组织的，以及其公开 source map 中嵌入了哪些源码级信息。

它并不声称与 Anthropic 内部开发仓库完全一致。文件边界、目录路径、生成产物和构建上下文都可能与原始私有源码树不同。

## 来源说明

当前快照严格建立在公开分发渠道之上：

- 公开 npm 包：[`@anthropic-ai/claude-code@2.1.88`](https://www.npmjs.com/package/@anthropic-ai/claude-code)
- 公开包元数据：[`package/package.json`](./package/package.json)
- 包内公开 source map：[`package/cli.js.map`](./package/cli.js.map)
- 本仓库附带的提取脚本：[`extract-sources.js`](./extract-sources.js)

根据本仓库内 `cli.js.map` 实测：

- 版本号：`2.1.88`
- `sources` 条目数：`4,756`
- 含 `sourcesContent` 的条目数：`4,756`

## 仓库结构

- [`package/`](./package/)：解包后的公开 npm 包内容
- [`src/`](./src/)：用于阅读和分析的重建源码快照
- [`extract-sources.js`](./extract-sources.js)：展示如何从 `sourcesContent` 中提取源码
- [`claude-code-2.1.88.tgz`](./claude-code-2.1.88.tgz)：本工作区保留的原始公开 tarball 快照

## 重建方式

高层流程很直接：

1. 获取目标版本的公开 npm tarball。
2. 读取该公开包内附带的 `cli.js.map`。
3. 从 source map 的 `sourcesContent` 条目中提取文件内容。
4. 将恢复出的内容写回可阅读的源码树，供分析使用。

也就是说，这个仓库建立在公开分发产物之上，而不是来自任何私有开发系统的特权访问。

## 使用边界

本仓库适合用于：

- 研究公开包结构
- 比较不同发布版本
- 检查 source map 中打包进去的内容
- 分析互操作性和打包行为

本仓库不用于：

- 取代官方 Claude Code 分发渠道
- 暗示 Anthropic 的赞助、认可或合作关系
- 鼓励对商标、品牌或版权材料的不当使用
- 保证当前重建树完整、可构建，或与原始内部仓库完全一致

## 权利与合规提示

- 仓库级权利说明见 [`LICENSE.md`](./LICENSE.md)
- 原始包内附带 [`package/LICENSE.md`](./package/LICENSE.md)，其中说明该软件受 Anthropic 相关法律协议约束。
- 官方产品、法律与合规信息应以 Anthropic 官方页面为准，而不是以本镜像为准。
- 若你是相关权利人，并认为某些文件或段落不应继续保留，请通过仓库托管平台联系维护者处理。

官方参考链接：

- [Claude Code 产品页](https://claude.com/product/claude-code)
- [Claude Code 文档](https://code.claude.com/docs/en/overview)
- [Anthropic 法律与合规说明](https://code.claude.com/docs/en/legal-and-compliance)

## 阅读建议

如果你准备引用或使用本仓库内容，建议按“公开产物研究快照”来理解：

- 讨论结论时优先引用原始公开包版本
- 行为判断尽量回到官方分发二进制或官方文档复核
- 不要把本仓库表述为官方源码仓库
- 下游再分发或二次发布前，先走你自己的法律与合规审查流程
