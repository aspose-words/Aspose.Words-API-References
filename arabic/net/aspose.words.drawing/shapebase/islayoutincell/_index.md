---
title: ShapeBase.IsLayoutInCell
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على أو تعيين علامة تشير إلى ما إذا كان الشكل معروضًا داخل الجدول أم خارجه.
type: docs
weight: 310
url: /ar/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

الحصول على أو تعيين علامة تشير إلى ما إذا كان الشكل معروضًا داخل الجدول أم خارجه.

```csharp
public bool IsLayoutInCell { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`حقيقي`.

له تأثير فقط على الأشكال ذات المستوى الأعلى، الخاصية[`WrapType`](../wraptype/) والتي تم ضبطها على value بخلاف[`Inline`](../../../aspose.words/inline/).

### أمثلة

يوضح كيفية تحديد كيفية عرض شكل في خلية جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 10;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Single;

table.Style = tableStyle;

builder.MoveTo(table.FirstRow.FirstCell.FirstParagraph);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);

// اضبط الخاصية "IsLayoutInCell" على "true" لعرض الشكل كعنصر سطري داخل فقرة الخلية.
// الأصل الإحداثي الذي سيحدد موقع الشكل سيكون في الزاوية العلوية اليسرى من خلية الشكل.
// إذا قمنا بإعادة حجم الخلية، فسيتحرك الشكل ليحافظ على نفس الموضع بدءًا من أعلى يسار الخلية.
// اضبط خاصية "IsLayoutInCell" على "خطأ" لعرض الشكل كشكل عائم مستقل.
// الأصل الإحداثي الذي سيحدد موقع الشكل سيكون في الزاوية العلوية اليسرى من الصفحة،
// ولن يستجيب الشكل لأي تغيير في حجم خليته.
shape.IsLayoutInCell = isLayoutInCell;

// يمكننا فقط تطبيق خاصية "IsLayoutInCell" على الأشكال العائمة.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


