# 用法

```
name: Github Forks Sync actio 

on:
  workflow_dispatch:
  
  schedule:
    - cron: 0 */12 * * *
	
jobs:
  Github-Forks-Sync-actio:
    runs-on: ubuntu-latest
    steps:
      - name: Github Forks Sync actio
        uses: GWen124/Github-Forks-Sync-action@master
        with:
          github_token: ${{ secrets.REPO_TOKEN }} # 令牌
          upstream_repository: luolongfei/freenom  # 上游仓库
          upstream_branch: master  # 默认是拉取上游仓库的master分支
          target_repository: leicancun/freenom  # 你要推送的仓库
          target_branch: master  # 默认推送到你的仓库master分支
          force: true  # 是否强制推送
          tags: false  # 确定是否使用-tags
```

# 感谢
### 项目来自<a href="https://github.com/TobKed">TobKed</a>：<a href="https://github.com/TobKed/github-forks-sync-action">github forks sync action</a>