---
title: VisitorAction Enum
linktitle: VisitorAction
articleTitle: VisitorAction
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.VisitorAction 枚举以轻松管理节点枚举，提高文档处理效率和控制力。
type: docs
weight: 7470
url: /zh/net/aspose.words/visitoraction/
---
## VisitorAction enumeration

允许访问者控制节点的枚举。

```csharp
public enum VisitorAction
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Continue | `0` | 访客请求继续枚举。 |
| SkipThisNode | `1` | 访问者请求跳过当前节点并继续枚举。 |
| Stop | `2` | 访问者请求停止节点枚举。 |

## 例子

展示如何使用文档访问器处理绝对位置制表符。

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // 通过接受这个自定义文档访问者来提取我们文档的文本内容。
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // 仅访问文档主体的开头。
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // 仅访问文档主体的末尾。
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // 绝对位置制表符，在字符串形式中没有等效项，已明确转换为制表符。
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // AbsolutePositionTab 本身也可以接受 DocumentVisitor。
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// 收集访问文档中所有运行的文本内容。将所有绝对制表符替换为普通制表符。
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 AbsolutePositionTab 节点时调用。
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将文本添加到当前输出。遵守启用/禁用输出标志。
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// 访问者积累的文档的纯文本。
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
