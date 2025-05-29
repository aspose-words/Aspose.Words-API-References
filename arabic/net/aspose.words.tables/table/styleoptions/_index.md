---
title: Table.StyleOptions
linktitle: StyleOptions
articleTitle: StyleOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Table StyleOptions لتخصيص مظهر جدولك باستخدام علامات بت مرنة. حسّن مظهر جدولك بسهولة!
type: docs
weight: 300
url: /ar/net/aspose.words.tables/table/styleoptions/
---
## Table.StyleOptions property

يحصل على أو يعين علامات البت التي تحدد كيفية تطبيق نمط الجدول على هذا الجدول.

```csharp
public TableStyleOptions StyleOptions { get; set; }
```

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

### أنظر أيضا

* enum [TableStyleOptions](../../tablestyleoptions/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
