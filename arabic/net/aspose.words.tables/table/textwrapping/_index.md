---
title: Table.TextWrapping
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. يحصل على أو مجموعاتTextWrapping للجدول.
type: docs
weight: 310
url: /ar/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

يحصل على أو مجموعات`TextWrapping` للجدول.

```csharp
public TextWrapping TextWrapping { get; set; }
```

### أمثلة

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

// قم بتعيين خاصية "TextWrapping" على "TextWrapping.Around" لجعل الجدول يلتف النص حوله،
// وادفعه للأسفل إلى الفقرة أدناه عن طريق تحديد الموضع.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### أنظر أيضا

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


