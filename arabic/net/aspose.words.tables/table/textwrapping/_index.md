---
title: Table.TextWrapping
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "التفاف النص في الجدول" لإدارة تدفق النص بسهولة في جداولك. حسّن سهولة القراءة والتصميم مع خيارات نص مرنة!
type: docs
weight: 310
url: /ar/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

يحصل أو يعين`TextWrapping` للجدول.

```csharp
public TextWrapping TextWrapping { get; set; }
```

## أمثلة

يوضح كيفية العمل مع التفاف نص الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بتعيين خاصية "TextWrapping" إلى "TextWrapping.Around" لجعل الجدول يلتف حول النص،
// ثم ادفعه إلى الأسفل في الفقرة أدناه عن طريق تعيين الموضع.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### أنظر أيضا

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
