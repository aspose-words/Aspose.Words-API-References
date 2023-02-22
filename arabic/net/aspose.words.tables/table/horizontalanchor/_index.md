---
title: Table.HorizontalAnchor
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. الحصول على الكائن الأساسي الذي يجب من خلاله حساب الموضع الأفقي للجدول العائم. القيمة الافتراضية هيColumn .
type: docs
weight: 170
url: /ar/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

الحصول على الكائن الأساسي الذي يجب من خلاله حساب الموضع الأفقي للجدول العائم. القيمة الافتراضية هيColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

### أمثلة

يوضح كيفية استخدام خصائص الجداول العائمة.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // فقط الهامش والصفحة والعمود متاحان في RelativeHorizontalPosition for HorizontalAnchor setter.
    // سيتم طرح ArgumentException لأية قيم أخرى.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // فقط الهامش والصفحة والفقرة المتوفرة في RelativeVerticalPosition لـ VerticalAnchor setter.
    // سيتم طرح ArgumentException لأية قيم أخرى.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### أنظر أيضا

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


