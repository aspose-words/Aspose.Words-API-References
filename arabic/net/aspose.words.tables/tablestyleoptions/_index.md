---
title: TableStyleOptions
second_title: Aspose.Words لمراجع .NET API
description: يحدد كيفية تطبيق نمط الجدول على الجدول .
type: docs
weight: 6070
url: /ar/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

يحدد كيفية تطبيق نمط الجدول على الجدول .

```csharp
[Flags]
public enum TableStyleOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تطبيق تنسيق نمط الجدول. |
| FirstRow | `20` | تطبيق التنسيق الشرطي للصف الأول ._ x000d_ |
| LastRow | `40` | تطبيق التنسيق الشرطي للصف الأخير ._ x000d_ |
| FirstColumn | `80` | تطبيق التنسيق الشرطي الأول للعمود الأول. |
| LastColumn | `100` | تطبيق التنسيق الشرطي للعمود الأخير ._ x000d_ |
| RowBands | `200` | تطبيق التنسيق الشرطي لربط الصفوف ._ x000d_ |
| ColumnBands | `400` | تطبيق التنسيق الشرطي لنطاقات الأعمدة ._ x000d_ |
| Default2003 | `600` | يتم تطبيق نطاقات الصفوف والأعمدة. هذا هو Microsoft Word الافتراضي للتنسيقات القديمة مثل DOC و WML و RTF. |
| Default | `2A0` | هذه هي الإعدادات الافتراضية لـ Microsoft Word . |

### أمثلة

يوضح كيفية إنشاء جدول جديد أثناء تطبيق النمط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// يجب علينا إدراج صف واحد على الأقل قبل تعيين أي تنسيق للجدول.
builder.InsertCell();

// تعيين نمط الجدول المستخدم بناءً على معرف النمط.
// لاحظ أنه ليست كل أنماط الجدول متاحة عند الحفظ بتنسيق doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// قم بتطبيق النمط جزئيًا على ميزات الجدول بناءً على المسندات ، ثم قم ببناء الجدول.
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

* property [StyleOptions](../table/styleoptions)
* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->