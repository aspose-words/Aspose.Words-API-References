---
title: ShapeBase.IsGroup
linktitle: IsGroup
articleTitle: IsGroup
second_title: .NET için Aspose.Words
description: ShapeBase IsGroup'u keşfedin. Bir şeklin grup olup olmadığını kolayca belirleyin. Daha iyi organizasyon için bu temel özellik ile tasarım iş akışınızı geliştirin.
type: docs
weight: 280
url: /tr/net/aspose.words.drawing/shapebase/isgroup/
---
## ShapeBase.IsGroup property

Geri Döndürür`doğru` eğer bu bir grup şekliyse.

```csharp
public bool IsGroup { get; }
```

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

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
