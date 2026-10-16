---
name: verify-before-stop
enabled: true
event: stop
action: warn
---

⚠️ **验证提醒（红线 #12）**

任务结束前请确认：
- 代码任务 → 跑了 test/lint/build 吗？
- PPT 任务 → 跑了 visual_review.py 吗？
- 搜索任务 → 确认了下载文件的分辨率和内容吗？
- 文件修改 → 确认了改动正确吗？

**不能只声明成功，必须有验证证据。**
