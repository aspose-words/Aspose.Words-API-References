---
title: AbsolutePositionTab.Accept
linktitle: Accept
articleTitle: Accept
second_title: 用于 .NET 的 Aspose.Words
description: AbsolutePositionTab Accept 方法. 接受访客 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问该节点的访问者。 |

### 返回值

`错误的`如果访问者请求停止枚举。

## 评论

通话[`VisitAbsolutePositionTab`](../../documentvisitor/visitabsolutepositiontab/)。

有关更多信息，请参阅访客设计模式。

## 例子

演示如何使用文档访问者处理绝对位置制表符。

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // 通过接受此自定义文档访问者来提取文档的文本内容。
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // 绝对位置制表符在字符串形式中没有等效项，已被显式转换为制表符。
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
    /// 在文档中遇到 AbsolutePositionTab 节点时调用。
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将文本添加到当前输出。尊重启用/禁用输出标志。
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

* class [DocumentVisitor](../../documentvisitor/)
* class [AbsolutePositionTab](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
