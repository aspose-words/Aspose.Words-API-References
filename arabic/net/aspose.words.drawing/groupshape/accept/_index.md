---
title: GroupShape.Accept
second_title: Aspose.Words لمراجع .NET API
description: GroupShape طريقة. يقبل الزائر.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/groupshape/accept/
---
## GroupShape.Accept method

يقبل الزائر.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيزور العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد؛ كاذبة إذا[`DocumentVisitor`](../../../aspose.words/documentvisitor/) أوقفت العملية قبل زيارة كافة العقد.

### ملاحظات

يعدد هذه العقدة وجميع أبنائها. تستدعي كل عقدة الطريقة المقابلة لها[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

لمزيد من المعلومات، راجع نمط تصميم الزائر.

المكالمات[`VisitGroupShapeStart`](../../../aspose.words/documentvisitor/visitgroupshapestart/) ، ثم يتصل[`Accept`](../../../aspose.words/node/accept/) لجميع الأشكال الفرعية لشكل المجموعة واستدعاءاتها[`VisitGroupShapeEnd`](../../../aspose.words/documentvisitor/visitgroupshapeend/) في النهاية.

### أمثلة

يوضح كيفية إنشاء مجموعة من الأشكال، وطباعة محتوياتها باستخدام زائر المستند.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // إذا كنت بحاجة إلى إنشاء أشكال "NonPrimitive"، مثل SingleCornerSnipped، وTopCornersSnipped، وDiagonalCornerSnipped،
    // TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، DiagonalCornersRounded
    // يرجى استخدام أساليب DocumentBuilder.InsertShape.
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
/// يطبع محتويات مجموعة الأشكال التي تمت زيارتها إلى وحدة التحكم.
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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../groupshape/)
* المجسم [Aspose.Words](../../../)


