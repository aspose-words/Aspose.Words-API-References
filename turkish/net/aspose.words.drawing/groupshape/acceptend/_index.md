---
title: GroupShape.AcceptEnd
linktitle: AcceptEnd
articleTitle: AcceptEnd
second_title: .NET için Aspose.Words
description: GroupShape AcceptEnd metodunu keşfedin, ziyaretçi etkileşimlerini sorunsuz bir şekilde yönetin ve bu güçlü özellik ile uygulamanızın kullanıcı deneyimini geliştirin.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/groupshape/acceptend/
---
## GroupShape.AcceptEnd method

GroupShape'in sonunu ziyaret eden bir ziyaretçiyi kabul eder.

```csharp
public override VisitorAction AcceptEnd(DocumentVisitor visitor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| visitor | DocumentVisitor | Belge ziyaretçisi. |

### Geri dönüş değeri

Ziyaretçinin yapması gereken eylem.

## Örnekler

Bir şekil grubunun nasıl oluşturulacağını ve içeriklerinin bir belge ziyaretçisi kullanılarak nasıl yazdırılacağını gösterir.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "İlkel Olmayan" şekiller oluşturmanız gerekiyorsa,
    // ÜstKöşelerBirYuvarlakBirKesilmiş, TekKöşeYuvarlak, ÜstKöşelerYuvarlak, ÇaprazKöşelerYuvarlak
    // Lütfen DocumentBuilder.InsertShape metotlarını kullanın.
    Shape balloon = new Shape(doc, ShapeType.Balloon)
    {
        Width = 200,
        Height = 200,
        Stroke = { Color = Color.Red }
    };

    Shape cube = new Shape(doc, ShapeType.Cube)
    {
        Width = 100,
        Height = 100,
        Stroke = { Color = Color.Blue }
    };

    GroupShape group = new GroupShape(doc);
    group.AppendChild(balloon);
    group.AppendChild(cube);

    Assert.True(group.IsGroup);

    builder.InsertNode(group);

    ShapeGroupPrinter printer = new ShapeGroupPrinter();
    group.Accept(printer);

    Console.WriteLine(printer.GetText());
}

/// <summary>
/// Ziyaret edilen şekil grubunun içeriğini konsola yazdırır.
/// </summary>
public class ShapeGroupPrinter : DocumentVisitor
{
    public ShapeGroupPrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        mBuilder.AppendLine("Shape group started:");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mBuilder.AppendLine("End of shape group");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeStart(Shape shape)
    {
        mBuilder.AppendLine("\tShape - " + shape.ShapeType + ":");
        mBuilder.AppendLine("\t\tWidth: " + shape.Width);
        mBuilder.AppendLine("\t\tHeight: " + shape.Height);
        mBuilder.AppendLine("\t\tStroke color: " + shape.Stroke.Color);
        mBuilder.AppendLine("\t\tFill color: " + shape.Fill.ForeColor);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mBuilder.AppendLine("\tEnd of shape");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
