---
name: warn-config-edits
enabled: true
event: file
action: warn
conditions:
  - field: file_path
    operator: regex_match
    pattern: settings\.json$|CLAUDE\.md$|MEMORY\.md$|gotchas\.md$
---

🔧 **系统配置文件修改中**

你正在编辑：`$FILE_PATH`

修改系统配置前请确认：
- 改后必须验证 JSON 语法（settings.json）
- 改 CLAUDE.md 红线前确认是"犯过 2 次的错"
- 改 MEMORY.md 保持 200 行以内
- 改后做一次自我检查：这个改动会让下次的我更聪明还是更困惑？
