# 4. 代码评审

## 参考资料

- [6 Ways to Quantify Your Code—and Why You Need to Do It](http://blog.newrelic.com/2014/12/16/quantify-your-code/)
- [让 Code Review 成为一种习惯](http://www.flickering.cn/uncategorized/2014/08/%E8%AE%A9-code-review%E6%88%90%E4%B8%BA%E4%B8%80%E7%A7%8D%E4%B9%A0%E6%83%AF/)
- [代码审查过程](http://blog.jobbole.com/84617/)

# 4.1 六种量化你代码的方式

本文为译文，译者为 Leo Hui(我自己！)。

Businesspeople dig numbers. They don’t necessarily want to hear that you got something done; they want to hear how much you got done—especially relative to past results or some other relevant benchmark—and they want to know the value of what you did.

商人关注的是量化，他们想从你哪里通道你做了什么，带来了什么价值，而不是你做了多少。

Some professionals have it easy when it comes to quantifying their job performance. Salespeople can measure their achievements in dollars and cents, for example, and many other fields also have clear-cut numbers with which to calculate their contributions.

教授可以轻松地量化出他们的工作，销售人员可以计算出他们的收益。其他的领域也可以通过一些方式算出他们的贡献。

For software developers and some other technology-based roles, however, quantifying your work can be a struggle without a straightforward solution. Yet doing so is crucial not just in job searches, but in many aspects of a software engineer’s career: performance reviews, effectively communicating up the chain of command, working efficiently with non-technical business units, and ensuring you’re properly valued within your organization.

但是从事软件开发以及技术相关的人员，量化工作确实一个困难的事情。量化这件事情，不是在求职，更是一个技术人员生涯的一部分。绩效评估，有效的了解沟通，高效的和非技术人员合作，确保你再团队或组织中的价值。

So how do you measure the value of the applications you build, scale, monitor, test, and otherwise support? Here are some of the approaches used at New Relic, as well as industry best practices:

但是我们要如何量化工作中的价值呢？这里有一些 New Relic 推荐的做法：

“I like to see work accomplishments described in terms of situation, action and results,” says Merilee Krebs, a technical recruiter at New Relic. “What was the business or technical problem to be solved?  What unique actions did you take to resolve them and what was the resulting improvement.”

New Relic 的技术招聘人员这样说："我喜欢看到用情况，行动和结果去描述工作成果， 技术人员需要解决的问题是什么？采用什么样的行动去解决和提升这个问题。"

What does that look like in the real world? Try asking yourself some pointed questions: Did your monitoring and testing lead to a code update that cut down on help desk tickets by X percent? That’s quantitative gold right there. Did you deliver a new app six weeks ahead of schedule? Yeah, you’ll want to brag about that (in a professional manner, of course). Can you connect your code to strategic company objectives? Please, do so. Are you doing something that’s outperforming the traditional standards in your industry? You should be able to quantify the achievement is some way.

现实世界中是怎样的呢？你试着问自己一些关键的问题：你有在更新你的代码的时候去监控和测试...这就是量化的目标。如果你在日程表前六周就完成了一个 app，你肯定会去炫耀一下。但是你有考虑公司的战略目标吗，如果没有，请思考一下。...

If this exercise feels unnatural to you, you’re not alone—many programmers often aren’t born sales and marketing pros. If they were, they’d probably work in sales or marketing. So let’s consider six ways to better measure and communicate the value of your code and related work.

你是不是感受到一些不同的感觉，这不是你一个人的问题，技术人员的通病。如果技术人员做好了量化这一块，那么他们也许就去从事销售了。所以，让我们考虑六种去量化你代码以及工作的方式：

- Think in percentages

- Get involved with open source projects

- Measure progress, not just products

- Keep a work journal

- Communicate in two languages

- Collect recommendations

## 参考资料

- [6 Ways to Quantify Your Code—and Why You Need to Do It](http://blog.newrelic.com/2014/12/16/quantify-your-code/)

# 4.2 程序员必备的代码审查（Code Review）清单
在我们关于高效代码审查的博文中，我们建议使用一个检查清单。在代码审查中，检查清单是一个非常好的工具——它们保证了审查可以在你的团队中始终如一的进行。它们也是一种保证常见问题能够被发现并被解决的便利方式。

软件工程学院的研究表明，程序员们会犯15-20种常见的错误。所以，通过把这些错误加入到检查清单当中，你可以确保不论什么时候，只要这些错误发生了，你就能发现它们，并且可以帮助你杜绝这些错误。

为了帮助你开始创建一个清单，这里列出了一些典型的内容：代码审查清单。

## 常规项

- 代码能够工作么？它有没有实现预期的功能，逻辑是否正确等。
- 所有的代码是否简单易懂？
- 代码符合你所遵循的编程规范么？这通常包括大括号的位置，变量名和函数名，行的长度，缩进，格式和注释。
- 是否存在多余的或是重复的代码？
- 代码是否尽可能的模块化了？
- 是否有可以被替换的全局变量？
- 是否有被注释掉的代码？
- 循环是否设置了长度和正确的终止条件？
- 是否有可以被库函数替代的代码？
- 是否有可以删除的日志或调试代码？

## 安全

- 所有的数据输入是否都进行了检查（检测正确的类型，长度，格式和范围）并且进行了编码？
- 在哪里使用了第三方工具，返回的错误是否被捕获？
- 输出的值是否进行了检查并且编码？
- 无效的参数值是否能够处理？

## 文档

- 是否有注释，并且描述了代码的意图？
- 所有的函数都有注释吗？
- 对非常规行为和边界情况处理是否有描述？
- 第三方库的使用和函数是否有文档？
- 数据结构和计量单位是否进行了解释？
- 是否有未完成的代码？如果是的话，是不是应该移除，或者用合适的标记进行标记比如‘TODO’？

## 测试

- 代码是否可以测试？比如，不要添加太多的或是隐藏的依赖关系，不能够初始化对象，测试框架可以使用方法等。
- 是否存在测试，它们是否可以被理解？比如，至少达到你满意的代码覆盖(code coverage)。
- 单元测试是否真正的测试了代码是否可以完成预期的功能？
- 是否检查了数组的“越界“错误？
- 是否有可以被已经存在的API所替代的测试代码？

## 总结

你同样需要把特定语言中有可能引起错误的问题添加到清单中。

这个清单故意没有详尽的列出所有可能会发生的错误。你不希望你的清单是这样的，太长了以至于从来没人会去用它。仅仅包含常见的问题会比较好。

## 优化你的清单

把使用清单作为你的起点，针对特定的使用案例，你需要对其进行优化。一个比较棒的方式就是让你的团队记录下那些在代码审查过程中临时发现的问题，有了这些数据，你就能够确定你的团队常犯的错误，然后你就可以量身定制一个审查清单。确保你删除了那些没有出现过的错误。（你也可以保留那些出现概率很小，但是非常关键的项目，比如安全相关的问题）。

## 得到认可并且保持更新

基本规则是，清单上的任何条目都必须明确，而且，如果可能的话，对于一些条目你可以对其进行二元判定。这样可以防止判断的不一致。和你的团队分享这份清单并且让他们认同你清单的内容是个好主意。同样的，要定期检查你的清单，以确保各条目仍然是有意义的。

有了一个好的清单，可以提高你在代码审查过程中发现的缺陷个数。这可以帮助你提高代码标准，避免质量参差不齐的代码审查。

## 参考资料

- [程序员必备的代码审查（Code Review）清单](http://blog.jobbole.com/83595/)