---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words لـ .NET
description: ShapeBase AllowOverlap ملكية. الحصول على أو تعيين القيمة التي تحدد ما إذا كان هذا الشكل يمكن أن يتداخل مع الأشكال الأخرى في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

الحصول على أو تعيين القيمة التي تحدد ما إذا كان هذا الشكل يمكن أن يتداخل مع الأشكال الأخرى.

```csharp
public bool AllowOverlap { get; set; }
```

## ملاحظات

تؤثر هذه الخاصية على سلوك الشكل في Microsoft Word. Aspose.Words يتجاهل قيمة هذه الخاصية.

تنطبق هذه الخاصية فقط على الأشكال ذات المستوى الأعلى.

القيمة الافتراضية هي`حقيقي`.

## أمثلة

يوضح كيفية العمل مع خصائص الجداول العائمة.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // يتوفر الهامش والصفحة والعمود فقط في RelativeHorizontalPosition لأداة ضبط HorizontalAnchor.
    // سيتم طرح ArgumentException لأي قيم أخرى.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // يتوفر فقط الهامش والصفحة والفقرة في RelativeVerticalPosition لأداة إعداد VerticalAnchor.
    // سيتم طرح ArgumentException لأي قيم أخرى.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
