---
title: GroupShape.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GroupShape AcceptStart للترحيب بالزائرين بسلاسة وتعزيز تجربتهم منذ بداية تطبيقك.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/groupshape/acceptstart/
---
## GroupShape.AcceptStart method

يقبل زائرًا لزيارة بداية GroupShape.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | زائر الوثيقة. |

### قيمة الإرجاع

الإجراء الذي يجب على الزائر اتخاذه.

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

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
