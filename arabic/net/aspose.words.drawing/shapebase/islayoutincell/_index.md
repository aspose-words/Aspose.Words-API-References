---
title: ShapeBase.IsLayoutInCell
linktitle: IsLayoutInCell
articleTitle: IsLayoutInCell
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase IsLayoutInCell، وتحكم في وضع الشكل في الجداول لتحسين مرونة التصميم وإدارة التخطيط.
type: docs
weight: 330
url: /ar/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

يحصل على علم أو يعينه للإشارة إلى ما إذا كان الشكل معروضًا داخل جدول أو خارجه.

```csharp
public bool IsLayoutInCell { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي`.

له تأثير فقط على الأشكال ذات المستوى الأعلى، الخاصية[`WrapType`](../wraptype/) منها ما تم ضبطه على value بخلاف[`Inline`](../../../aspose.words/inline/).

## أمثلة

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

// قم بضبط الخاصية "IsLayoutInCell" على "true" لعرض الشكل كعنصر مضمن داخل فقرة الخلية.
// سيكون أصل الإحداثيات الذي سيحدد موقع الشكل هو الزاوية العلوية اليسرى لخلية الشكل.
// إذا قمنا بتغيير حجم الخلية، فسوف يتحرك الشكل للحفاظ على نفس الموضع بدءًا من أعلى يسار الخلية.
// اضبط خاصية "IsLayoutInCell" على "false" لعرض الشكل كشكل عائم مستقل.
// سيكون أصل الإحداثيات الذي سيحدد موقع الشكل هو الزاوية العلوية اليسرى من الصفحة،
// ولن يستجيب الشكل لأي تغيير في حجم خليته.
shape.IsLayoutInCell = isLayoutInCell;

// يمكننا فقط تطبيق الخاصية "IsLayoutInCell" على الأشكال العائمة.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
