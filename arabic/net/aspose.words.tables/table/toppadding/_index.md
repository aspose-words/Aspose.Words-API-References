---
title: Table.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table TopPadding، واضبط المساحة بسهولة في النقاط الموجودة أعلى محتويات الخلية لتحسين التحكم في التخطيط وتحسين إمكانية القراءة.
type: docs
weight: 330
url: /ar/net/aspose.words.tables/table/toppadding/
---
## Table.TopPadding property

يحصل على مقدار المساحة (بالنقاط) المراد إضافتها فوق محتويات الخلايا أو يعينه.

```csharp
public double TopPadding { get; set; }
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
