---
title: DocumentVisitor.VisitFieldSeparator
linktitle: VisitFieldSeparator
articleTitle: VisitFieldSeparator
second_title: Aspose.Words for .NET
description: 探索 DocumentVisitor 中的 VisitFieldSeparator 方法。高效处理文档中的字段分隔符，从而简化处理流程。
type: docs
weight: 190
url: /zh/net/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor.VisitFieldSeparator method

当在文档中遇到字段分隔符时调用。

```csharp
public virtual VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldSeparator | FieldSeparator | 正在访问的对象。 |

### 返回值

一个[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

## 评论

字段分隔符用于分隔文档中的字段代码和字段值。请注意，某些 字段只有字段代码，没有字段分隔符和字段值。

有关详细信息，请参阅[`VisitFieldStart`](../visitfieldstart/)

## 例子

展示如何打印文档中每个字段的节点结构。

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者会访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点非二叉树。
/// 以字符串的形式创建所有遇到的 Field 节点及其子节点的映射。
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 FieldStart 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 FieldEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 FieldSeparator 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 向 StringBuilder 追加一行，并根据访问者的深度进行缩进
    /// 进入字段的子节点树。
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* enum [VisitorAction](../../visitoraction/)
* class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* class [DocumentVisitor](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
