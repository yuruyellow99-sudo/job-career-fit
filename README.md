# job-career-fit

寻找自己的职业匹配方向，并且帮你对意向岗位评分

一个面向求职者的 Codex Skill，结合工作案例访谈、职业方向探索和 JD 匹配。适合想弄清楚自己能迁移什么能力、哪些行业和业务线值得看，以及具体岗位入职后会做什么的人。

## 能做什么

- 从简历和工作案例提炼可验证的能力，了解候选人希望继续做什么、下一步想积累什么。
- 先给可在 BOSS 直聘、智联招聘和猎聘复制的岗位搜索词，再按行业、城市、公司和业务线列出相应岗位。
- 可接入 `boss-zhipin-scraper`，按城市和关键词多页采集岗位与薪资，再按岗位去重、补读 JD。也支持使用该工具导出的职位文件。
- 对照 JD 和简历评估岗位匹配度，核实岗位职责、业务归属和薪资口径。岗位匹配度达到高档时，按上传的原版格式自动生成一页定向简历。
- 评估公司与行业对个人发展的价值。国家和地方政策、大额投资等主张有可靠、可追溯来源才计分。

## 在 Codex 中使用

下载或克隆此仓库，把包含 `SKILL.md` 和 `references/` 的 `job-career-fit` 文件夹放入 `~/.agents/skills/`。如只想在一个项目中使用，可放入该项目的 `.agents/skills/`。已安装的用户可更新本地克隆，或重新复制最新版技能文件夹。如果技能未出现在选择器里，重启 Codex。

### 探索职业方向

```text
$job-career-fit 根据我的简历和一个工作案例，先问我想积累什么，再推荐主选、备选和次备选行业。
```

### 查岗位和薪资

```text
$job-career-fit 在XX和XX找研发侧整机系统工程师和机器人系统集成工程师。先列搜索词，再在 BOSS 直聘按城市和关键词多页搜索，给出公司、岗位原名、薪资、来源和待核实项。
```

实时查询 BOSS 直聘需要另行安装 [boss-zhipin-scraper](https://github.com/eatmoreduck/boss-zhipin-scraper)，并在其专用浏览器中登录。按抓取工具的 `SKILL.md` 执行环境检查。若 Codex 内启动浏览器时遇到系统权限错误，可在普通系统终端按抓取工具的说明启动专用浏览器，再回到 Codex 检查连接。你也可以上传已有的 JSON 或 CSV 导出；实时连接不可用时，结果会注明替代来源。详见 [BOSS 直聘数据接入](references/boss-data-source.md)。

### 评估 JD 并自动生成一页简历

```text
$job-career-fit 评估这个 JD。给出岗位与简历匹配度、团队可能负责的业务、公开薪资和待核实的问题。符合高匹配条件时，按我上传的原版生成一页定向简历。
```

一并上传原版简历并提供完整 JD 或岗位链接。默认在岗位与简历的匹配度达到 **4/5 或 5/5**、评分有充分证据且无已确认的硬性条件冲突时生成本地草稿。原版为 PDF 时，默认交付版式尽量一致、文字可选中的单页 PDF。只想评估时，可以在提示词里写「只评估，暂不改简历」。详情见 [一页定向简历](references/one-page-resume.md) 和 [调研与评分规则](references/research-and-scoring.md)。

## 致谢与许可

批量岗位初筛和逐条简历举证的设计参考了 [ai-job-search](https://github.com/ai-job-search-dev/ai-job-search) 与 [career-ops](https://github.com/career-ops-hq/career-ops)。BOSS 直聘数据来自独立项目 [boss-zhipin-scraper](https://github.com/eatmoreduck/boss-zhipin-scraper) 或招聘页。本项目采用 [MIT License](LICENSE)。
