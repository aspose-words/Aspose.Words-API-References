---
title: Shape.StrokeColor
linktitle: StrokeColor
articleTitle: StrokeColor
second_title: .NET için Aspose.Words
description: Shape StrokeColor özelliğiyle tasarımınızı özelleştirerek çarpıcı görsel etki için canlı vuruş renkleri tanımlayabilirsiniz.
type: docs
weight: 200
url: /tr/net/aspose.words.drawing/shape/strokecolor/
---
## Shape.StrokeColor property

Bir vuruşun rengini tanımlar.

```csharp
public Color StrokeColor { get; set; }
```

## Notlar

Bu, şuna giden bir kısayoldur:[`Color`](../../stroke/color/) mülk.

Varsayılan değer Black .

## Örnekler

Bir şeklin düz bir renkle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Biraz metin yazın ve ardından onu yüzen bir şekille örtün.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Şeklin dış hatlarının rengini ayarlamak için "StrokeColor" özelliğini kullanın.
shape.StrokeColor = Color.CadetBlue;

// Şeklin iç alanının rengini ayarlamak için "FillColor" özelliğini kullanın.
shape.FillColor = Color.LightBlue;

// "Opaklık" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak, 0 ise görünmez anlamına gelir.
// Şeklin dolgusu varsayılan olarak tamamen opak olduğundan, şeklin üstündeki metni göremeyiz.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Şeklin dolgu renginin opaklığını daha düşük bir değere ayarlayın, böylece altındaki metni görebiliriz.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

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

* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
