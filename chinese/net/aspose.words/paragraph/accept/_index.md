---
title: Paragraph.Accept
second_title: Aspose.Words for .NET API 参考
description: Paragraph 方法. 接受访客
type: docs
weight: 230
url: /zh/net/aspose.words/paragraph/accept/
---
## Paragraph.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为 True；假如果[`DocumentVisitor`](../../documentvisitor/)在访问所有节点之前停止操作。

### 评论

枚举该节点及其所有子节点。每个节点调用相应的方法[`DocumentVisitor`](../../documentvisitor/)。

有关更多信息，请参阅访客设计模式。

通话[`VisitParagraphStart`](../../documentvisitor/visitparagraphstart/)，然后调用[`Accept`](../../node/accept/)对于该段落的所有子节点 并调用[`VisitParagraphEnd`](../../documentvisitor/visitparagraphend/)最后.

### 例子

演示如何使用 DocumentVisitor 实现从文档中删除所有隐藏内容。

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // 以下是可以接受文档访问者的三种类型的字段，
    // 这将允许它访问接受节点，然后以深度优先的方式遍历其子节点。
    // 1 - 段落节点：
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - 表节点：
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - 文档节点：
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// 删除所有标记为“隐藏内容”的已访问节点。
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// 在文档中遇到 FieldStart 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 FieldEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 FieldSeparator 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到段落节点时调用。
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 FormField 时调用。
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 GroupShape 时调用。
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Shape 时调用。
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到注释时调用。
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到脚注时调用。
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到特殊字符时调用。
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 文档中Table节点访问结束时调用。
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // 表格单元格内的内容可能具有隐藏内容标志，但表格本身不能。
        // 如果该表只有隐藏内容，则该访问者将删除所有内容，
        // 这样就不会剩下任何子节点了。
        // 因此，我们也可以将表格本身视为隐藏内容并将其删除。
        // 为空但没有隐藏内容的表格将具有内部带有空段落的单元格，
        // 该访问者不会删除它。
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 文档中某个Cell节点的访问结束时调用。
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 文档中Row节点访问结束时调用。
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### 也可以看看

* class [DocumentVisitor](../../documentvisitor/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../paragraph/)
* 部件 [Aspose.Words](../../../)


