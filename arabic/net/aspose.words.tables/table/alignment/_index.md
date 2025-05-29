---
title: Table.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية محاذاة الجدول للتحكم بسهولة في وضع الجدول المضمن في مستنداتك للحصول على مظهر أنيق واحترافي.
type: docs
weight: 40
url: /ar/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

يحدد كيفية محاذاة جدول مضمن في المستند.

```csharp
public TableAlignment Alignment { get; set; }
```

## ملاحظات

القيمة الافتراضية هيLeft.

## أمثلة

يوضح كيفية تطبيق حدود تفصيلية على جدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

//محاذاة الجدول إلى منتصف الصفحة.
table.Alignment = TableAlignment.Center;

// قم بمسح أي حدود وتظليل موجود من الجدول.
table.ClearBorders();
table.ClearShading();

//أضف حدودًا خضراء إلى مخطط الجدول.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// املأ الخلايا بلون أخضر فاتح.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### أنظر أيضا

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
