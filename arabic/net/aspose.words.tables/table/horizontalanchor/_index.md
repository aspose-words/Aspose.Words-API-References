---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words لـ .NET
description: Table HorizontalAnchor ملكية. يحصل على الكائن الأساسي الذي يجب حساب الموضع الأفقي للجدول العائم منه. القيمة الافتراضية هيColumn  في C#.
type: docs
weight: 170
url: /ar/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

يحصل على الكائن الأساسي الذي يجب حساب الموضع الأفقي للجدول العائم منه. القيمة الافتراضية هيColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
