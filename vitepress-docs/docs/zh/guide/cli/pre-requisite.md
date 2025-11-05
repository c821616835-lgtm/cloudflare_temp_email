# 先决条件

## wrangler 的安装

安装 wrangler

```bash
npm install wrangler -g
```

## 克隆项目

```bash
git clone https://github.com/dreamhunter2333/cloudflare_temp_email.git
# 切换到最新 tag 或者你想部署的分支，你也可以直接使用 main 分支
# git checkout $(git describe --tags $(git rev-list --tags --max-count=1))
```
cd worker
cp wrangler.toml.template wrangler.toml
# 创建 D1 并执行 schema.sql
wrangler d1 create dev
wrangler d1 execute dev --file=../db/schema.sql --remote
