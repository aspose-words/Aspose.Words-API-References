---
title: DocumentVisitor.VisitOfficeMathStart
second_title: Aspose.Words for .NET API 参考
description: DocumentVisitor 方法. 在开始枚举 Office Math 对象时调用
type: docs
weight: 310
url: /zh/net/aspose.words/documentvisitor/visitofficemathstart/
---
## DocumentVisitor.VisitOfficeMathStart method

在开始枚举 Office Math 对象时调用。

```csharp
public virtual VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| officeMath | OfficeMath | 正在访问的对象。 |

### 返回值

A[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

### 例子

演示如何打印文档中每个 Office Math 节点的节点结构。

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问过的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点的非二叉树。
/// 以字符串形式创建所有遇到的 OfficeMath 节点及其子节点的映射。
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
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
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 OfficeMath 节点时调用。
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问 OfficeMath 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

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

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* enum [VisitorAction](../../visitoraction/)
* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [DocumentVisitor](../)
* 命名空间 [Aspose.Words](../../documentvisitor/)
* 部件 [Aspose.Words](../../../)


