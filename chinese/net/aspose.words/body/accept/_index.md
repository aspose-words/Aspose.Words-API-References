---
title: Body.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: 探索 Body Accept 方法，实现无缝访客互动。我们独特的方法提升用户体验，提升转化率！
type: docs
weight: 40
url: /zh/net/aspose.words/body/accept/
---
## Body.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为 True；如果访问了所有节点，则为 false[`DocumentVisitor`](../../documentvisitor/)在访问所有节点之前停止操作。

## 评论

枚举此节点及其所有子节点。每个节点都会调用相应的方法[`DocumentVisitor`](../../documentvisitor/)。

欲了解更多信息，请参阅访客设计模式。

呼叫[`VisitBodyStart`](../../documentvisitor/visitbodystart/)，然后调用[`Accept`](../../node/accept/)对于 section 的所有子节点并调用[`VisitBodyEnd`](../../documentvisitor/visitbodyend/)在最后。

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

* class [DocumentVisitor](../../documentvisitor/)
* class [Body](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
