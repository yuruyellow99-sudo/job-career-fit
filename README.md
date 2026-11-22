# job-career-fit

寻找自己的职业匹配方向，并且帮你对岗位评分

一个面向求职者的 Codex Skill，结合工作案例访谈、职业方向探索和 JD 匹配。适合想弄清楚自己能迁移什么能力、哪些行业和业务线值得看，以及具体岗位入职后会做什么的人。

## 能做什么

- 从简历和工作案例提炼可验证的能力，了解候选人希望继续做什么、下一步想积累什么。
- 按行业、城市和业务线推荐企业，并给出可在 BOSS 直聘、智联招聘和猎聘使用的岗位搜索词。
- 对照 JD 和简历评估匹配度，核实岗位职责、业务归属和薪资口径。
- 评估公司与行业对个人发展的价值。国家和地方政策、大额投资等主张有可靠、可追溯来源才计分。

## 在 Codex 中使用

下载或克隆此仓库，把包含 `SKILL.md` 和 `references/` 的 `job-career-fit` 文件夹放入 `~/.agents/skills/`。如只想在一个项目中使用，可放入该项目的 `.agents/skills/`。如果技能未出现在选择器里，重启 Codex。

示例提示词

```text
$job-career-fit 根据我的简历和一个工作案例，先问我想积累什么，再推荐主选、备选和次备选行业。
```

```text
$job-career-fit 评估这个 JD。给出岗位与简历匹配度、团队可能负责的业务、公开薪资和待核实的问题。
```

技能规则见 [SKILL.md](SKILL.md)，调研和评分细节见 [research-and-scoring.md](references/research-and-scoring.md)。

## 致谢与许可

批量岗位初筛和逐条简历举证的设计参考了 [ai-job-search](https://github.com/ai-job-search-dev/ai-job-search) 与 [career-ops](https://github.com/career-ops-hq/career-ops)。本项目采用 [MIT License](LICENSE)。
