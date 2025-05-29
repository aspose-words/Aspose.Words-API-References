---
title: DocumentVisitor.VisitGroupShapeEnd
linktitle: VisitGroupShapeEnd
articleTitle: VisitGroupShapeEnd
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة DocumentVisitor VisitGroupShapeEnd، التي تشير بشكل فعال إلى نهاية تعداد شكل المجموعة لمعالجة المستندات بشكل سلس.
type: docs
weight: 260
url: /ar/net/aspose.words/documentvisitor/visitgroupshapeend/
---
## DocumentVisitor.VisitGroupShapeEnd method

يتم استدعاؤها عند انتهاء تعداد شكل المجموعة.

```csharp
public virtual VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| groupShape | GroupShape | الشيء الذي يتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية مواصلة التعداد.

## أمثلة

يوضح كيفية إنشاء مجموعة من الأشكال وطباعة محتوياتها باستخدام زائر المستند.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // إذا كنت بحاجة إلى إنشاء أشكال "غير بدائية"، مثل SingleCornerSnipped وTopCornersSnipped وDiagonalCornersSnipped،
    // الزوايا العلوية مستديرة واحدة، زوايا علوية مستديرة واحدة، زوايا علوية مستديرة، زوايا قطرية مستديرة
    // يرجى استخدام طرق DocumentBuilder.InsertShape.
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
/// طباعة محتويات مجموعة الأشكال التي تمت زيارتها في وحدة التحكم.
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

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
