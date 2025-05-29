---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية AllowOverlap في ShapeBase، وقم بالتحكم في تفاعلات الأشكال عن طريق تمكين أو تعطيل التداخل مع الأشكال الأخرى لتحسين مرونة التصميم.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

يحصل على قيمة تحدد ما إذا كان هذا الشكل يمكنه التداخل مع الأشكال الأخرى أو يعينها.

```csharp
public bool AllowOverlap { get; set; }
```

## ملاحظات

تؤثر هذه الخاصية على سلوك الشكل في Microsoft Word. يتجاهل Aspose.Words قيمة هذه الخاصية.

تنطبق هذه الخاصية على الأشكال ذات المستوى الأعلى فقط.

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

    // فقط الهامش والصفحة والعمود متاح في RelativeHorizontalPosition لمحدد HorizontalAnchor.
    //سيتم طرح ArgumentException لأي قيم أخرى.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // فقط الهامش والصفحة والفقرة متاحة في RelativeVerticalPosition لمحدد VerticalAnchor.
    //سيتم طرح ArgumentException لأي قيم أخرى.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
