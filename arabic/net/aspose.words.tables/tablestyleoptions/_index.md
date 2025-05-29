---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words.Tables.TableStyleOptions لتصميم جداول مرن. حسّن تصميم مستندك بأنماط جداول قابلة للتخصيص اليوم!
type: docs
weight: 7220
url: /ar/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

يحدد كيفية تطبيق نمط الجدول على جدول.

```csharp
[Flags]
public enum TableStyleOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تطبيق تنسيق نمط الجدول. |
| FirstRow | `20` | تطبيق التنسيق الشرطي للصف الأول. |
| LastRow | `40` | تطبيق التنسيق الشرطي للصف الأخير. |
| FirstColumn | `80` | تطبيق التنسيق الشرطي للعمود الأول. |
| LastColumn | `100` | تطبيق التنسيق الشرطي للعمود الأخير. |
| RowBands | `200` | تطبيق التنسيق الشرطي لربط الصفوف. |
| ColumnBands | `400` | تطبيق التنسيق الشرطي لنطاقات الأعمدة. |
| Default2003 | `600` | تم تطبيق توزيع الصفوف والأعمدة. هذا هو الوضع الافتراضي في مايكروسوفت وورد للتنسيقات القديمة مثل DOC وWML وRTF. |
| Default | `2A0` | هذه هي الإعدادات الافتراضية لبرنامج Microsoft Word. |

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

* property [StyleOptions](../table/styleoptions/)
* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
