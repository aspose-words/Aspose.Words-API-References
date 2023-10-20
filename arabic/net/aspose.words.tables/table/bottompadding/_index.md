---
title: Table.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words لـ .NET
description: Table BottomPadding ملكية. الحصول على أو تعيين مقدار المسافة بالنقاط لإضافتها أسفل محتويات الخلايا في C#.
type: docs
weight: 90
url: /ar/net/aspose.words.tables/table/bottompadding/
---
## Table.BottomPadding property

الحصول على أو تعيين مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات الخلايا.

```csharp
public double BottomPadding { get; set; }
```

## أمثلة

يوضح كيفية تكوين حشوة المحتوى في الجدول.

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
// سيحافظ هذا الجدول على الحد الأدنى من مسافة الحشو عن طريق التفاف النص.
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
