---
title: Table.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table LeftPadding، وقم بتعديل مسافة محتوى الخلية بسهولة بالنقاط لتحسين التحكم في التخطيط وتحسين مرونة التصميم.
type: docs
weight: 200
url: /ar/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

يحصل على مقدار المساحة (بالنقاط) التي يجب إضافتها إلى يسار محتويات الخلايا أو يعينها.

```csharp
public double LeftPadding { get; set; }
```

## أمثلة

يوضح كيفية تكوين تعبئة المحتوى في جدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // لكل خلية في الجدول، قم بتعيين المسافة بين محتوياتها وكل حدودها.
// سيحافظ هذا الجدول على الحد الأدنى لمسافة الحشو عن طريق لف النص.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
