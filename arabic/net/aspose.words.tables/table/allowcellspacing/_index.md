---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table AllowCellSpacing لإدارة مسافات الخلايا بسهولة في تخطيطاتك. حسّن تصميمك بخيارات قابلة للتخصيص!
type: docs
weight: 60
url: /ar/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

يحصل على خيار "السماح بالتباعد بين الخلايا" أو يعينه.

```csharp
public bool AllowCellSpacing { get; set; }
```

## أمثلة

يوضح كيفية تمكين المسافة بين الخلايا الفردية في جدول.

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
// بحجم يساوي قيمة خاصية "CellSpacing"، بالنقاط.
// اضبط خاصية "AllowCellSpacing" على "false" لتعطيل تباعد الخلايا
// وتجاهل قيمة الخاصية "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// سيؤدي تعديل خاصية "CellSpacing" إلى تمكين تباعد الخلايا تلقائيًا.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
