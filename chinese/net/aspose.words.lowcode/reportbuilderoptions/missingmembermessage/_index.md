---
title: ReportBuilderOptions.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words for .NET
description: 探索 ReportBuilderOptions 的 MissingMemberMessage 属性。轻松自定义缺失对象引用的消息，轻松提升用户体验。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/reportbuilderoptions/missingmembermessage/
---
## ReportBuilderOptions.MissingMemberMessage property

获取或设置打印的字符串值，而不是模板表达式，该值表示对对象缺失成员的简单引用。默认值为空字符串。

```csharp
public string MissingMemberMessage { get; set; }
```

## 评论

该属性应与AllowMissingMembers 选项。否则，当遇到对象缺少成员时会引发异常。

此属性仅影响表示对 missing 对象成员的普通引用的模板表达式的打印。例如，打印二元运算符（其中一个操作数引用 missing 对象成员）不受影响。

此属性的值不能设置为 null。

### 也可以看看

* class [ReportBuilderOptions](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
