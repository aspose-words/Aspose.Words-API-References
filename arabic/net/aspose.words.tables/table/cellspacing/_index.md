---
title: Table.CellSpacing
linktitle: CellSpacing
articleTitle: CellSpacing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table CellSpacing لتخصيص مسافة الخلايا بسهولة بالنقاط، مما يعزز مظهر الجدول وقابليته للقراءة.
type: docs
weight: 100
url: /ar/net/aspose.words.tables/table/cellspacing/
---
## Table.CellSpacing property

يحصل على مقدار المساحة (بالنقاط) بين الخلايا أو يعينها.

```csharp
public double CellSpacing { get; set; }
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

يوضح كيفية إنشاء إعدادات نمط مخصصة للجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

//قد يؤثر تعيين خصائص نمط الجدول على خصائص الجدول نفسه.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
