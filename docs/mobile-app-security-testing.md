# 移动应用安全测试:工具和最佳实践

> 原文：<https://circleci.com/blog/mobile-app-security-testing/>

为了最大限度地降低应用程序的安全风险，开发人员需要他们的应用程序经得起严格的安全测试。幸运的是，有一些工具可以简化甚至自动化这些安全测试。还有最佳实践来指导和通知测试过程。

在本文中，我将介绍移动应用程序最常见的安全问题，并重点介绍流行的安全测试。我还将讨论移动应用安全测试的最佳实践，并回顾在 CI/CD 管道中保护移动应用的工具。

## 移动应用安全测试的重要性

为了理解为什么安全测试很重要，我将描述这些常见问题:

*   数据存储保护不当
*   使用本机代码引起的内存问题
*   使用开源/第三方工具

### 数据存储保护不当

如果您没有为您的数据库设置适当的数据库凭证，或者如果您的 cookie 存储加密不良，攻击者可以很容易地读取这些数据存储的内容。

以根设备或逆向工程应用程序为例。如果由于安全措施薄弱，攻击者可以轻松地访问您的数据库，那么您的信息就有被泄露的风险。

### 使用本机代码引起的内存问题

尽管用 C、C++和 Objective-C 编写的应用程序要快得多，但是用这些语言编写的糟糕的代码会导致内存泄漏和缓冲区溢出。这些内存陷阱会导致 RAM 的问题以及内核-陆地进程的系统稳定性问题。攻击者可能利用这些问题来执行其他攻击，甚至通过触发内存泄漏和缓冲区溢出来导致拒绝服务(DoS)攻击。

使用[通用 C 编程](https://developer.ibm.com/articles/au-toughgame/)和 [Objective-C](https://spin.atomicobject.com/2017/01/22/avoiding-objective-c-memory-leaks/) 中的最佳实践来避免内存泄漏。静态代码测试(在运行代码之前检查应用程序中的安全漏洞)有助于更早地识别此类威胁。静态代码测试工具可以查明哪里可能发生内存泄漏和缓冲区溢出。

### 使用开源/第三方工具

开发人员使用开源库和框架来简化代码生产是很常见的。攻击者可以使用这些工具对您的系统发起攻击。更糟糕的是，当在应用程序中使用时，它们可能会启动恶意代码。

导致客户数据泄露的开源漏洞的一个例子是 [ParkMobile 漏洞](https://krebsonsecurity.com/2021/04/parkmobile-breach-exposes-license-plate-data-mobile-numbers-of-21m-users/)。一个第三方软件漏洞泄露了这个流行的北美停车应用程序的 2100 万用户的个人信息。

第三方服务漏洞通常是错误配置的结果。Check Point Research 发现 [1 亿用户](https://research.checkpoint.com/2021/mobile-app-developers-misconfiguration-of-third-party-services-leave-personal-data-of-over-100-million-exposed/)的私人数据因集成使用不当而暴露。

左移测试方法是避免第三方风险的最有效方法。这种方法强调在应用程序开发生命周期的开始就设置测试。Shift-left 允许测试您打算使用的开源和第三方工具的漏洞。这将有助于你及时发现危险信号。

## 安全性测试的重要性

对你的应用的攻击可能对你的组织不利。安全性测试对开发生命周期非常重要，因为它:

*   使您的应用符合行业标准。
*   让你的终端用户对你的产品产生信任感(例如，当你的应用通过 ISO 27001 认证时)。
*   帮助您检测和了解弱点，以便您能够消除和防范安全漏洞等风险。
*   降低与安全事故相关的成本，包括财务成本和声誉成本。
*   帮助您了解应用生态系统中需要调整的内容:第三方代码、您的代码或您的安全人员。

## 安全测试的类型

在本节中，我将探讨几种类型的移动应用程序安全性测试:

*   漏洞扫描
*   渗透测试
*   风险评估
*   姿势评估

### 漏洞扫描

这种方法使用自动化工具来检查应用生态系统中可能在攻击过程中受到危害的区域。漏洞扫描器寻找已知的漏洞，尤其是软件依赖关系中的漏洞。

漏洞扫描还可以检测应用程序中容易遗漏的漏洞，检查常见漏洞及其特征的记录。然后将匹配情况报告给开发人员或质量保证(QA)团队。您可以将漏洞扫描集成到 CI 管道中，我将在本文后面介绍这一点。

### 渗透测试

渗透测试模拟攻击来测试应用程序的安全性并找出其弱点。这不同于漏洞扫描，因为它涉及到人工输入(在这种情况下，是一个有道德的黑客)。他们使用多种技术侵入应用程序，检查攻击者可能利用的地方。

与漏洞扫描不同，漏洞扫描会导致误报，而渗透测试识别的威胁是真实的。这些测试通常可以提供漏洞精确位置的更多细节。

### 风险评估

风险评估包括列出应用生态系统中的所有组件和人员，以确定他们在遭受网络攻击时的个人风险。这有助于对组织内的某些资产实施措施，例如，如果 IT 部门的某人决定帮助或煽动攻击。

### 姿势评估

状态评估确定应用程序的当前安全状态，帮助开发人员确定需要改进的地方。它可以告诉您在攻击过程中哪些信息可能会受到损害，它将如何中断业务，需要多长时间才能恢复，以及需要采取哪些预防措施。

状态和风险评估一起工作，它们也可能包含其他类型的安全测试。所有这些都有一个共同的目标，那就是帮助您识别安全漏洞、防止攻击并减轻攻击。

## 移动应用安全测试的最佳实践

在本节中，我们将探讨保护和测试移动应用安全性的最佳实践的优势。这些是

*   供应链测试
*   使用 SAST、DAST 和 IAST 的技术
*   认证和认证测试
*   加密测试

### 供应链测试

攻击者可能不会直接攻击你的应用程序的主要代码，但他们可能会使用第三方代码。安全问题一节中讨论的开源和不可信的第三方工具就属于这一类。防止这些攻击的一种方法是左移测试，前面也讨论过。更具体地说，您可以执行静态代码测试，这可以通过静态应用程序安全测试(SAST)工具轻松实现。正如我们将在下一节中看到的，这些工具可以帮助检测安全风险。

供应链测试可以防止最终用户开始使用你的应用时出现的安全风险。使用其他方法进行测试时，供应链风险很容易被遗漏或忽略。

### 使用 SAST、DAST 和 IAST 的技术

SAST 指的是在应用程序运行之前测试应用程序代码的漏洞。Klocwork 和 Checkmarx 等工具对于实现 SAST 非常有用。

动态应用安全测试(DAST)主要针对运行中的应用。DAST 扫描应用程序以检查任何可能导致安全风险的漏洞。用于移动设备的 DAST 工具的一个例子是 HCL AppScan。

交互式应用安全测试(IAST)融合了 SAST 和 DAST 的特点，从而最大限度地发挥优势，最小化权衡。IAST 有助于捕捉源代码中和运行时的漏洞。

您可以使用这三种技术来帮助您轻松地识别可能发生诸如内存泄漏和缓冲区溢出、不正确的输入验证等问题的地方。查看 [SAST vs DAST:它们是什么以及何时使用它们](https://circleci.com/blog/sast-vs-dast-when-to-use-them/)了解这些技术的更多信息。

### 认证和认证测试

薄弱的身份验证和授权允许攻击者获得更高的权限，并做出可能导致系统崩溃或收集用户信用数据的事情。DAST 有助于确保用户不会在不该登录或不该访问的时候登录应用程序。

以共享目录为例。拥有学生权限的用户能否访问只有拥有教师权限的用户才能访问的答案文件？用户可以绕过安全问题检查吗？在做测试的时候，这些问题应该在你的脑海中。

### 加密测试

强大的加密算法将使攻击者很难访问应用程序并获得重要信息。注意，仅在授权上设置加密是不够的。作为开发人员，我们可能会忘记或忽略在我们的应用程序使用的层中设置它，并且可能包含敏感信息。例如，OSI 模型的传输层。攻击者可以使用传输层进行窃听、泄露通信信息等。

为了确保您的应用程序遵循加密的最佳实践，请使用 SAST 来确保您设置了强大的加密机制。

## 在您的测试中使用持续集成

尽管安全测试很重要，但在许多开发团队中并不总是优先考虑。许多开发者更关注于实现应用的主要目标。应用程序中有许多需要测试的漏洞，您可能无法手动发现。如果开发人员发现安全测试浪费他们的时间，他们倾向于跳过它。

为了防止这种情况，您可以通过在 CI/CD 管道中设置安全测试工具来使用测试自动化。这些工具可用于向开发人员反馈关于应用程序漏洞的有意义的数据，开发人员反过来处理这些数据。开发人员可以专注于应用程序的交付，同时修复漏洞。

## 用于保护 CI/CD 管道中的移动应用的工具

要将测试集成到移动应用程序的 CI/CD 管道中，您可以使用 [CircleCI 的移动测试工具。](https://circleci.com/blog/mobile-and-browser-testing-on-circleci-simple-setup-easy-management-increased-confidence/)

多亏了 orbs，在这个平台上设置和管理测试很容易。orb 是一种可重用的 YAML 配置，有助于自动化重复的过程。使用 orbs 可以简化项目设置。您可以在 CircleCI 管道中轻松使用可信的第三方安全测试提供者。

一些有用的 orb，可以共享 CircleCI 配置的包，包括 [NowSecure](https://circleci.com/developer/orbs/orb/nowsecure/ci-auto-orb) 和 [Genymotion](https://circleci.com/developer/orbs/orb/genymotion/genymotion-saas) 。

## 结论

移动应用程序的广泛用户基础使它们对攻击者更具吸引力。此外，第三方应用程序的不当配置等安全问题会使它们更容易受到攻击。

现在，您已经了解了漏洞扫描和状态评估等安全测试，以及遵循最佳实践的重要性，您可以确保您的应用和用户的个人数据得到保护。

[联系 CircleCI](https://circleci.com/contact/) 了解有关将安全测试添加到您的移动应用的 CI/CD 管道的更多信息。