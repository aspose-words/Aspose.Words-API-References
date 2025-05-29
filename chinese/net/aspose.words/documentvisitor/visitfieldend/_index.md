---
title: DocumentVisitor.VisitFieldEnd
linktitle: VisitFieldEnd
articleTitle: VisitFieldEnd
second_title: Aspose.Words for .NET
description: 探索 DocumentVisitor 的 VisitFieldEnd 方法，该方法对于处理文档中的字段终止至关重要。立即提升您的编码效率！
type: docs
weight: 180
url: /zh/net/aspose.words/documentvisitor/visitfieldend/
---
## DocumentVisitor.VisitFieldEnd method

当文档中的字段结束时调用。

```csharp
public virtual VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldEnd | FieldEnd | 正在访问的对象。 |

### 返回值

一个[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

## 评论

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
* class [FieldEnd](../../../aspose.words.fields/fieldend/)
* class [DocumentVisitor](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
