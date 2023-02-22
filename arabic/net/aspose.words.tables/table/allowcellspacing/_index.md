---
title: Table.AllowCellSpacing
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. الحصول على أو تعيين خيار السماح بالتباعد بين الخلايا.
type: docs
weight: 60
url: /ar/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

الحصول على أو تعيين خيار "السماح بالتباعد بين الخلايا".

```csharp
public bool AllowCellSpacing { get; set; }
```

### أمثلة

يوضح كيفية تمكين التباعد بين الخلايا الفردية في جدول.

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

// اضبط خاصية "AllowCellSpacing" على "true" لتمكين التباعد بين الخلايا
// بقيمة مساوية لقيمة خاصية "CellSpacing" بالنقاط.
// اضبط خاصية "AllowCellSpacing" على "false" لتعطيل تباعد الخلايا
// وتجاهل قيمة خاصية "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// سيؤدي ضبط خاصية "CellSpacing" تلقائيًا إلى تمكين تباعد الخلايا.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


