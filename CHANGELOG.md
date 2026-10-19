# 母版变更记录

## 2.3.6 - 公开维护候选（2026-10-19）

- 为通用维护合同与 opt-in `pi-goal-operator` Skill 0.1.3 增加容量/写域/恢复判据；明确这是操作约定，不是运行时预算或恢复执行器。
- 保持十个数学 Skill 激活入口、既有单文件/PR差异上限和发布扫描策略不变；新增 builder 打包回归，验证维护 Skill 仍随模板复制且不进入数学激活 allowlist。
- 保留顶层研究激励与现有仓库身份；不修改数学研究记录、actor、Goal 或实际预算。
- 修复维护差异门身份绑定：CI 以稳定 `GITHUB_ACTOR_ID` 判定维护权限，登录名只作诊断；缺失/不匹配时 fail closed，`--actor-id` 仅是本地测试上下文；普通 Web candidate 规则不变。
- 单独提出的完整 2.4.1 参考库候选仍 HOLD，未包含在本版或描述为已发布。

回滚：使用普通 revert 回退 2.3.6 维护文档和 opt-in Skill 更新；不改写已发布历史或影响运行中的 actor/Goal。

## 2.3.5 - 候选（2026-10-01）

- `pi-goal-x@0.31.9` MIT 原版与 MIT 项目补丁分别固定摘要；`scripts/install_goal_patch.py` 在官方 Pi 项目安装后仅接受受审前镜像或目标镜像。默认隐藏 Goal 面板但不改变原生续行、Esc/暂停/恢复；`/goal-snapshot` 仅有明确配置时桥接 `sealed-pair-shadow.v1`，母版现存 checkpoint reporter **不**提供兼容 owner。
- `.pi/extensions/goal-context.ts` 默认惰性，显式绑定受信 session/cwd 时保留 Pi 原生 compaction 语义并仅压缩历史文件清单的重复呈现；`scripts/goal_shadow_bridge.py`/`goal_snapshot_store.py` 保存经 owner checksum 与附件字节校验的候选双文档，恢复到新目录，不产生 Evidence/Result。
- `VERSION`、source manifest、snapshot 与同仓历史同步升级；安装/代码、进程已加载及数学准入分别验收。本模板不启动任何研究 actor。
- 候选复核修正：安装器接受文档中的 `--project-root .`，但仍拒绝符号链接/词法越界；协作安装由 advisory lock 协调，源树在 promotion 前再次核对字节及 inode/时间，后半程读回失败会隔离当前镜像并尽力恢复原件。受审包根与子成员均须为本人拥有、不可被组/其他人写入的真实目录/普通文件；源镜像不可信时不自动 chmod 或覆盖。断电双 rename 窗口与非协作 writer 最终窗口有明确人工恢复边界，不宣称事务原子性。

回滚：使用正常 revert PR 回到 2.3.4 快照和补丁前版本；不要删除历史条目或修改运行中的 Goal/会话/研究目录。
