---
name: block-dangerous-ops
enabled: true
event: bash
action: block
conditions:
  - field: command
    operator: regex_match
    pattern: rm\s+-rf\s+/[^t]|rm\s+-rf\s+~|rm\s+-rf\s+\$HOME|git\s+push\s+--force\s+origin\s+(main|master)
---

🚫 **危险操作已拦截**

命令被阻止：`$COMMAND`

如果确认要执行，请：
- 确认路径完全正确
- 确认有备份
- 先用 `echo` 或 `ls` 验证目标路径
