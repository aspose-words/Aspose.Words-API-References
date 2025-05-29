---
title: Shape.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: 探索 Shape Accept 方法，旨在增强访客参与度并简化您的接受流程以获得更好的结果。
type: docs
weight: 250
url: /zh/net/aspose.words.drawing/shape/accept/
---
## Shape.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为 True；如果访问了所有节点，则为 false[`DocumentVisitor`](../../../aspose.words/documentvisitor/)在访问所有节点之前停止操作。

## 评论

枚举此节点及其所有子节点。每个节点都会调用相应的方法[`DocumentVisitor`](../../../aspose.words/documentvisitor/)。

欲了解更多信息，请参阅访客设计模式。

呼叫[`VisitShapeStart`](../../../aspose.words/documentvisitor/visitshapestart/)，然后调用[`Accept`](../../../aspose.words/node/accept/) 表示形状的所有子节点并调用[`VisitShapeEnd`](../../../aspose.words/documentvisitor/visitshapeend/)在最后。

## 例子

展示如何遍历文档中的所有形状。

```csharp
public void VisitShapes()
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 记录有关访问形状的外观相关信息。
/// </summary>
private class ShapeAppearancePrinter : DocumentVisitor
{
    public ShapeAppearancePrinter()
    {
        mShapesVisited = 0;
        mTextIndentLevel = 0;
        mStringBuilder = new StringBuilder();
    }

    /// <summary>
    /// 将一行附加到 StringBuilder，每个缩进级别前面都添加一个制表符。
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// 返回 StringBuilder 已累积的所有文本。
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// 当此访问者访问 Shape 节点的起点时调用。
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        AppendLine($"Shape found: {shape.ShapeType}");

        mTextIndentLevel++;

        if (shape.HasChart)
            AppendLine($"Has chart: {shape.Chart.Title.Text}");

        AppendLine($"Extrusion enabled: {shape.ExtrusionEnabled}");
        AppendLine($"Shadow enabled: {shape.ShadowEnabled}");
        AppendLine($"StoryType: {shape.StoryType}");

        if (shape.Stroked)
        {
            Assert.AreEqual(shape.Stroke.Color, shape.StrokeColor);
            AppendLine($"Stroke colors: {shape.Stroke.Color}, {shape.Stroke.Color2}");
            AppendLine($"Stroke weight: {shape.StrokeWeight}");
        }

        if (shape.Filled)
            AppendLine($"Filled: {shape.FillColor}");

        if (shape.OleFormat != null)
            AppendLine($"Ole found of type: {shape.OleFormat.ProgId}");

        if (shape.SignatureLine != null)
            AppendLine($"Found signature line for: {shape.SignatureLine.Signer}, {shape.SignatureLine.SignerTitle}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当此访问者访问 Shape 节点的末尾时调用。
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当此访问者访问 GroupShape 节点的起点时调用。
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当此访问者访问 GroupShape 节点的末尾时调用。
    /// </summary>
    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mTextIndentLevel--;
        AppendLine($"End of {groupShape.ShapeType}");

        return VisitorAction.Continue;
    }

    private int mShapesVisited;
    private int mTextIndentLevel;
    private readonly StringBuilder mStringBuilder;
}
```

### 也可以看看

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
