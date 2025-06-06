---
title: Shape.Chart
linktitle: Chart
articleTitle: Chart
second_title: .NET için Aspose.Words
description: Şekil Tablosu ile grafik özelliklerinin kilidini açın. Görsel veri sunumunuzu zahmetsizce geliştirin ve içgörülerinizi bugün en üst düzeye çıkarın!
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/shape/chart/
---
## Shape.Chart property

Bu şeklin bir özelliği varsa grafik özelliklerine erişim sağlar.[`Chart`](../../../aspose.words.drawing.charts/chart/) .

```csharp
public Chart Chart { get; }
```

## Notlar

Bu özellik şunu döndürecektir:[`Chart`](../../../aspose.words.drawing.charts/chart/) yalnızca nesne[`HasChart`](../haschart/) özelliği`doğru` bunun için[`Shape`](../), aksi takdirde bir istisna fırlatacaktır.

## Örnekler

Bir belgedeki tüm şekiller üzerinde nasıl yineleme yapılacağını gösterir.

```csharp
public void VisitShapes()
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Ziyaret edilen şekiller hakkında görünümle ilgili bilgileri kaydeder.
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
    /// Her girinti düzeyi için bir sekme karakterinin önüne eklendiği bir satırı StringBuilder'a ekler.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// StringBuilder'ın biriktirdiği tüm metni döndür.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Bu ziyaretçi bir Şekil düğümünün başlangıcını ziyaret ettiğinde çağrılır.
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
    /// Bu ziyaretçi bir Shape düğümünün sonunu ziyaret ettiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bu ziyaretçi bir GroupShape düğümünün başlangıcını ziyaret ettiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bu ziyaretçi bir GroupShape düğümünün sonunu ziyaret ettiğinde çağrılır.
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

### Ayrıca bakınız

* class [Chart](../../../aspose.words.drawing.charts/chart/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
