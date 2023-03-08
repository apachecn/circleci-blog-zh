# 如何在 CI/CD | CircleCI 上销售您的经理

> 原文：<https://circleci.com/blog/how-to-sell-your-team-on-ci-cd/>

持续集成似乎是一个明智的选择，对吗？为什么会有人认为尽快将你的代码集成到产品中是个坏主意？

让我带你回到 2000 年 8 月，当时一位年轻的工程师刚刚开始她的第一份工程工作。她得到了一张桌子、一台电脑和一份详细的项目计划，其中包括未来三个月的发布日期。当她写代码的时候，QA 工程师正忙着写测试计划，为发布候选做准备。

经过四个月的艰苦工作，工程师和她的团队将他们的代码发送到 CD-ROM 工厂，该工厂将打印 CD-r om 发送给客户。许多客户都在急切地等待这个软件的新版本。距离上一次更新已经过去了八个月，他们六个月前报告的 bug 开始让他们烦恼。

上面的故事是我对软件工程入门的真实描述。当时，更新软件的成本是巨大的。这需要很长的测试周期和大量的艰苦工作来确保文档的准确性——截图可能会很快过时，但文档在软件发布后无法更新。

对产品做出改变是困难的，而且犯错的代价也很高。

## CI/CD 的独特优势

今天，事情有了很大的不同，这主要归功于持续集成和持续交付(CI/CD)。

很难夸大能够在产品准备好的时候就做出改变的强大影响。工程师和客户之间的反馈回路要短得多，作为工程师，我们可以以把客户放在第一位的方式来回应客户的反馈。

降低向客户交付变更的成本意味着我们可以快速回滚我们引入的任何错误。这也意味着在进行以前看起来有风险的变革时有了更多的信心。一次引入一个变化也有助于避免那些在最后一刻将两个特性推到一起时难以发现的错误。

事实上，你可以通过不断的改变来获得更高质量的产品，这看起来似乎是违反直觉的，但是在现实中，这是改进的唯一方法。

那么，你对一个对 CI/CD 持怀疑态度的管理者说些什么呢？以下是您的经理可能会问的一些问题的潜在答案:

注意不要说一些类似于“尽可能快地将代码投入生产”的话来吓到你的经理

这可能会被理解为将未完成的或损坏的功能放在客户面前，但事实并非如此。一个好的答案可能是类似于这样的话，"[持续集成](https://circleci.com/continuous-integration/)是将我们的工作分成小块，与我们的同事分享我们的工作，并经常问答。"

## CI/CD 的成本是多少？

转移到 CI/CD 的成本取决于您愿意在伟大的自动化测试上投资多少。正因为如此，成本会随着你在测试过程中的进展而变化。如果您手动进行大部分或全部测试，成本可能会比您拥有一套丰富的自动化测试(包括端到端测试)更高。

投资自动化测试是很容易的。在 CI 工具上运行自动化测试比雇佣工程师做同样的事情花费更少，也更可靠。请注意，你是在要求你的经理用特性交付来抵消这个价值，这可能是一个艰难的决定。预计您的经理将希望逐步增加自动化测试，并可能在部署之前增加一个手动 QA 步骤——这是许多团队为了实现 CI/CD 而采取的步骤。

Life Pro 提示:如果你的经理问你 CI/CD 的价格，而你回答团队将花费多少季度，他们会更认真地对待你。

## 投资 CI/CD 有什么好处？

虽然我确信每个经理都在为他们的工程师的幸福投资——我知道我是——但很少有经理能够花费大量时间专门让他们的工程师幸福。是的，CI/CD 是一项伟大的投资，因为它使您的开发人员的工作更加愉快，但是工程师的快乐仅仅是一项伟大的商业决策的副作用。

CI/CD 还有许多好处，这些好处超越了工程师的快乐，真正证明了投资的合理性。

1.  对于多个团队成员来说，在同一个特性上工作要容易得多。
2.  合并小变更的成本比大变更低得多。
3.  团队成员可以在一个已经通过自动化测试的系统中评估他们同事的变更，而不是一个特性分支的移动目标。
4.  对于 QA 工程师来说，在一个一致的系统中迭代地验证小的变化要容易得多，因此检测错误的来源变得简单得多。
5.  功能可以在更早的状态下到达客户手中。这意味着，如果我们在错误的轨道上，我们可以在少量投资后改变方向。

## 与领导价值观保持一致，以获得 CI/CD 的“肯定”

作为工程师，我们知道 CI/CD 是有意义的。这意味着代码质量更高，功能交付更快。它在我们的产品代码中引入了一种信心，这种信心在特性被集成并在它们被编写之后很久才交付时是不存在的。

对一些经理来说，这可能感觉不直观。为了让你的经理接受 CI/CD，你需要使用符合他们价值观的语言和想法。希望这篇文章能提供一个好的起点。