# GitHub 每日热点仓库报告

自动汇总 GitHub 每日热点的中文报告，由 [Hermes Agent](https://hermes-agent.nousresearch.com/docs) 定时任务每天上午 9 点生成并提交。

## 目录结构

```
github-reports/
├── README.md
├── 2026-06/        # 月份目录
│   ├── 2026-06-25.md
│   ├── 2026-06-26.md
│   └── ...
└── 2026-07/
    ├── 2026-07-01.md
    └── ...
```

每个 `YYYY-MM/YYYY-MM-DD.md` 是当天的报告。

## 数据来源

- 数据采集：`/f/project/github_report/scripts/fetch_trending.py`
- 报告输出：`F:/docs/github-reports/`
- 定时任务：Hermes cron job `f406a9a1f450`（每天 9:00 Asia/Shanghai）

## 推送

GitHub 凭证使用 Windows Credential Manager（用户级），cron 在 fresh session 也能直接 push。
