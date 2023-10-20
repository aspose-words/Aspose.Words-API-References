---
title: Table.ClearShading
linktitle: ClearShading
articleTitle: ClearShading
second_title: Aspose.Words لـ .NET
description: Table ClearShading طريقة. إزالة كل التظليل الموجود على الطاولة في C#.
type: docs
weight: 380
url: /ar/net/aspose.words.tables/table/clearshading/
---
## Table.ClearShading method

إزالة كل التظليل الموجود على الطاولة.

```csharp
public void ClearShading()
```

## أمثلة

يوضح كيفية تطبيق حدود المخطط التفصيلي على جدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// قم بمحاذاة الجدول إلى منتصف الصفحة.
table.Alignment = TableAlignment.Center;

// امسح أي حدود وتظليل موجود من الجدول.
table.ClearBorders();
table.ClearShading();

// أضف حدودًا خضراء إلى مخطط الجدول.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// املأ الخلايا بلون أخضر فاتح خالص.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
