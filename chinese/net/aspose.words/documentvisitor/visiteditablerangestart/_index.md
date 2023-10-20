---
title: DocumentVisitor.VisitEditableRangeStart
linktitle: VisitEditableRangeStart
articleTitle: VisitEditableRangeStart
second_title: 用于 .NET 的 Aspose.Words
description: DocumentVisitor VisitEditableRangeStart 方法. 在文档中遇到可编辑范围的开头时调用 在 C#.
type: docs
weight: 170
url: /zh/net/aspose.words/documentvisitor/visiteditablerangestart/
---
## DocumentVisitor.VisitEditableRangeStart method

在文档中遇到可编辑范围的开头时调用。

```csharp
public virtual VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| editableRangeStart | EditableRangeStart | 正在访问的对象。 |

### 返回值

A[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

## 例子

演示如何打印文档中每个可编辑范围的节点结构。

```csharp
public void EditableRangeToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    EditableRangeStructurePrinter visitor = new EditableRangeStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问过的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点的非二叉树。
/// 以所有遇到的 EditableRange 节点及其子节点的字符串形式创建一个映射。
/// </summary>
public class EditableRangeStructurePrinter : DocumentVisitor
{
    public EditableRangeStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideEditableRange = false;
    }

    /// <summary>
    /// 获取访问者积累的文档的纯文本。
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        // 我们想要打印运行的内容，但前提是它们位于形状内部，就像文本框的情况一样
        if (mVisitorIsInsideEditableRange) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 EditableRange 节点时调用。
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        IndentAndAppendLine("[EditableRange start] ID: " + editableRangeStart.Id + " Owner: " +
                            editableRangeStart.EditableRange.SingleUser);
        mDocTraversalDepth++;
        mVisitorIsInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当EditableRange节点访问结束时调用。
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[EditableRange end]");
        mVisitorIsInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行追加到 StringBuilder 并根据访问者在文档树中的深度对其进行缩进。
    /// </summary>
    /// <param name="text"></param>;
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideEditableRange;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* enum [VisitorAction](../../visitoraction/)
* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentVisitor](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
