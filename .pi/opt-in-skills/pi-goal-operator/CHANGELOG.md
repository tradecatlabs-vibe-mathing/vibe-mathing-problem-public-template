# pi-goal-operator Changelog

## 0.1.3 - 2026-10-18

- 扩充既有维护合同，区分单文件/累计目录字节/文件数/物理容量/producer计算预算和真实写域授权；摘要不能扩大或收窄授权，已授权目录内分卷保留真实累计预算。
- 恢复验收要求同一actor出现新成功执行、原范围内持久写入与读回；状态、ACK或checkpoint自证不算恢复。新增五个离线容量/授权/恢复压力场景；不增加通用运行时防线。
- 回滚：普通回退本版文档和压力场景；不改变现有actor、Goal、文件或producer预算。

## 0.1.2 - 2026-10-01

- 安装维护契约现在区分固定 npm 原版与受审补丁缓存，说明默认隐藏面板与受限 `/goal-snapshot`，不授予数学研究能力。
- 回滚：只撤销本版说明，不动既有 actor/Goal；公共母版回滚用普通 revert PR。

## 0.1.1 - 2026-09-27

- 增加 Pi 本地安装缓存及维护进程误读存储根的场景：区分固定包安装、Git 忽略的可执行缓存与公开 Harness 源码；安装后仍要运行 `make check-full`，包摘要漂移或被强制跟踪必须停放。不能用另一存储根的空列表推断原 Goal 不存在。
- 回滚：撤销本版文档增量，不改变原有数学 actor、包版本或在线 Hook 防护。

## 0.1.0 - 2026-09-27

### Added
- 单问题 canonical actor 的 Pi Goal 身份核验、唯一调度、恢复和独立数学准入边界。
- 离线压力场景：包声明不等于加载、旧 Hook 护栏未替换、旧 dispatch 不重放、Goal 完成不等于数学闭合。

### Reason
- `pi-goal-x` 是扩展，不属于十个数学 Skills；维护者仍需要可显式加载、可审查的操作说明，不应污染数学 actor 的能力 allowlist。

### Affected
- `SKILL.md`、`references/pressure-tests.md`，及母版 `TEMPLATE_REPOSITORY.md` 中的维护者入口。

### Validation
- 用固定版本插件源码核对命令、调度和设置语义；母版生成与 validator 回归测试及显式 Pi Skill 加载测试在本轮执行。

### Rollback
- 恢复到原先只读 `TEMPLATE_REPOSITORY.md` 的维护方式，移除这个尚未激活的可选 Skill 与源清单中的整树条目；不要改变运行中的 Goal 或 Hook。
