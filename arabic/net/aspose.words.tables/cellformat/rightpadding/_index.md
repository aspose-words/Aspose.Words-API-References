---
title: CellFormat.RightPadding
second_title: Aspose.Words لمراجع .NET API
description: CellFormat ملكية. إرجاع أو تعيين مقدار المسافة بالنقاط المراد إضافتها إلى يمين محتويات الخلية.
type: docs
weight: 90
url: /ar/net/aspose.words.tables/cellformat/rightpadding/
---
## CellFormat.RightPadding property

إرجاع أو تعيين مقدار المسافة (بالنقاط) المراد إضافتها إلى يمين محتويات الخلية.

```csharp
public double RightPadding { get; set; }
```

### أمثلة

يوضح كيفية تنسيق الخلايا باستخدام أداة إنشاء المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// أدخل خلية ثانية، ثم قم بتكوين خيارات حشو نص الخلية.
// سيقوم المنشئ بتطبيق هذه الإعدادات في خليته الحالية، وسيتم إنشاء أي خلايا جديدة بعد ذلك.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// لم تتأثر الخلية الأولى بإعادة تكوين الحشو، ولا تزال تحتفظ بالقيم الافتراضية.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// ستستمر الخلية الأولى في النمو في مستند الإخراج لتتناسب مع حجم الخلية المجاورة لها.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### أنظر أيضا

* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../cellformat/)
* المجسم [Aspose.Words](../../../)


