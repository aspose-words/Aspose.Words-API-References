---
title: DocumentVisitor.VisitFieldStart
linktitle: VisitFieldStart
articleTitle: VisitFieldStart
second_title: 用于 .NET 的 Aspose.Words
description: DocumentVisitor VisitFieldStart 方法. 当字段在文档中开始时调用 在 C#.
type: docs
weight: 200
url: /zh/net/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor.VisitFieldStart method

当字段在文档中开始时调用。

```csharp
public virtual VisitorAction VisitFieldStart(FieldStart fieldStart)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldStart | FieldStart | 正在访问的对象。 |

### 返回值

A[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

## 评论

Word 文档中的字段由字段代码和字段值组成。

例如，显示页码的字段可以表示如下：

[字段开始]PAGE[字段分隔符]98[字段结束]

字段分隔符将文档中的字段代码与字段值分开。请注意，某些 字段只有字段代码，没有字段分隔符和字段值。

字段可以嵌套。

## 例子

演示如何打印文档中每个字段的节点结构。

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问过的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点的非二叉树。
/// 以字符串形式创建所有遇到的 Field 节点及其子节点的映射。
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
    /// 在文档中遇到 FieldStart 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 FieldEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 FieldSeparator 节点时调用。
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 向 StringBuilder 添加一行，并根据访问者的深度缩进它
    /// 进入字段的子节点树。
    /// </summary>
    /// <param name="text"></param>;
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
* class [FieldStart](../../../aspose.words.fields/fieldstart/)
* class [DocumentVisitor](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
