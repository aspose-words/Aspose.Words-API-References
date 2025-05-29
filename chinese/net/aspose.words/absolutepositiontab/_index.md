---
title: AbsolutePositionTab Class
linktitle: AbsolutePositionTab
articleTitle: AbsolutePositionTab
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.AbsolutePositionTab 类，可在 WordprocessingML 中实现精确的文本定位，从而增强文档格式和控制。
type: docs
weight: 120
url: /zh/net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

绝对位置制表符是用于在显示此 WordprocessingML 内容时推进当前文本行上的位置的字符。

要了解更多信息，请访问[Aspose.Words 文档对象模型（DOM）](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class AbsolutePositionTab : SpecialChar
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [Font](../../aspose.words/inline/font/) { get; } | 提供对此对象的字体格式的访问。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 返回`真的`如果此节点可以包含其他节点。 |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | 如果在启用更改跟踪的情况下 Microsoft Word 中的对象格式发生更改，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | 返回SpecialChar. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | 检索父级[`Paragraph`](../paragraph/)此节点的。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../range/)表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| override [GetText](../../aspose.words/specialchar/gettext/)() | 获取此节点代表的特殊字符。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

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

* class [SpecialChar](../specialchar/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
