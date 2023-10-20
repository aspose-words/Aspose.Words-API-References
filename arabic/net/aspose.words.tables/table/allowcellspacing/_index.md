---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words لـ .NET
description: Table AllowCellSpacing ملكية. الحصول على خيار السماح بالتباعد بين الخلايا أو تعيينه في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

الحصول على خيار "السماح بالتباعد بين الخلايا" أو تعيينه.

```csharp
public bool AllowCellSpacing { get; set; }
```

## أمثلة

يوضح كيفية تمكين التباعد بين الخلايا الفردية في الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// اضبط خاصية "AllowCellSpacing" على "صحيح" لتمكين التباعد بين الخلايا
// بحجم يساوي قيمة خاصية "CellSpacing" بالنقاط.
// اضبط خاصية "AllowCellSpacing" على "خطأ" لتعطيل تباعد الخلايا
// وتجاهل قيمة خاصية "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// سيؤدي ضبط خاصية "CellSpacing" إلى تمكين تباعد الخلايا تلقائيًا.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
