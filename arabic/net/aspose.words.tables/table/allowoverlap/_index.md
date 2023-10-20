---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words لـ .NET
description: Table AllowOverlap ملكية. يحصل على ما إذا كان الجدول العائم يسمح للكائنات العائمة الأخرى في المستند بتداخل نطاقاته عند عرضها. القيمة الافتراضية هيحقيقي  في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

يحصل على ما إذا كان الجدول العائم يسمح للكائنات العائمة الأخرى في المستند بتداخل نطاقاته عند عرضها. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool AllowOverlap { get; }
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

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
