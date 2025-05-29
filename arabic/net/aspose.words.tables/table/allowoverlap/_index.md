---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "السماح بالتداخل في الجدول"، التي تتحكم في إمكانية تداخل الكائنات العائمة مع جدولك. حسّن مرونة التخطيط لعرض أفضل للمستندات.
type: docs
weight: 70
url: /ar/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

يحصل على ما إذا كان الجدول العائم يسمح للأشياء العائمة الأخرى في المستند بالتداخل مع امتداداته عند عرضها. القيمة الافتراضية هي`حقيقي` .

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

    // فقط الهامش والصفحة والعمود متاح في RelativeHorizontalPosition لمحدد HorizontalAnchor.
    //سيتم طرح ArgumentException لأي قيم أخرى.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // فقط الهامش والصفحة والفقرة متاحة في RelativeVerticalPosition لمحدد VerticalAnchor.
    //سيتم طرح ArgumentException لأي قيم أخرى.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
