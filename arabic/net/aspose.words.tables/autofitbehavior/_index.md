---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
articleTitle: AutoFitBehavior
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Tables.AutoFitBehavior enum لتحسين تغيير حجم الجدول باستخدام طريقة AutoFit، وتحسين تخطيط المستند وعرضه.
type: docs
weight: 7080
url: /ar/net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

يحدد كيفية تغيير حجم الجدول بواسطة Aspose.Words عند استدعاء[`AutoFit`](../table/autofit/) الطريقة.

```csharp
public enum AutoFitBehavior
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| AutoFitToContents | `0` | يتيح Aspose.Words خيار AutoFit، ويزيل العرض المفضل من الجدول وجميع الخلايا ثم يقوم بتحديث تخطيط الجدول. |
| AutoFitToWindow | `1` | عند استخدام هذه القيمة، يقوم Aspose.Words بتمكين خيار AutoFit، ويضبط العرض المفضل للجدول إلى 100%، ويقوم بإزالة العرض المفضل من جميع الخلايا ثم يقوم بتحديث تخطيط الجدول. |
| FixedColumnWidths | `2` | يقوم Aspose.Words بتعطيل خيار AutoFit وإزالة المفضل من الجدول. |

## أمثلة

يوضح كيفية إنشاء جدول جديد أثناء تطبيق نمط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// يجب علينا إدراج صف واحد على الأقل قبل تعيين تنسيق أي جدول.
builder.InsertCell();

// قم بتعيين نمط الجدول المستخدم بناءً على معرف النمط.
// لاحظ أن أنماط الجدول ليست كلها متاحة عند الحفظ بتنسيق .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// قم بتطبيق النمط جزئيًا على ميزات الجدول استنادًا إلى المسندات، ثم قم ببناء الجدول.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

يوضح كيفية إنشاء جدول 2x2 منسق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// أثناء إنشاء الجدول، سيقوم منشئ المستند بتطبيق قيم خصائص RowFormat/CellFormat الحالية
// إلى الصف/الخلية الحالية التي يتواجد بها المؤشر وأي صفوف/خلايا جديدة أثناء إنشائها.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// لا تتأثر الصفوف والخلايا المضافة مسبقًا بأثر رجعي بالتغييرات التي تطرأ على تنسيق المنشئ.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
