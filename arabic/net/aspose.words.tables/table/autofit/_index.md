---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة "الضبط التلقائي للجداول" لتغيير حجم الجداول والخلايا بسهولة للحصول على تصميم مثالي. حسّن عرض مستندك بسهولة!
type: docs
weight: 380
url: /ar/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

تغيير حجم الجدول والخلايا وفقًا لسلوك الملاءمة التلقائية المحدد.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| behavior | AutoFitBehavior | يحدد كيفية ملاءمة الجدول تلقائيًا. |

## ملاحظات

تُحاكي هذه الطريقة الأوامر المتاحة في قائمة "التوافق التلقائي" لجدول في Microsoft Word. الأوامر المتاحة هي "التوافق التلقائي مع المحتويات" و"التوافق التلقائي مع النافذة" و"عرض العمود الثابت". في Microsoft Word ، تُعيّن هذه الأوامر خصائص الجدول ذات الصلة، ثم تُحدّث تخطيطه، ويقوم Aspose.Words بالمثل.

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

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
