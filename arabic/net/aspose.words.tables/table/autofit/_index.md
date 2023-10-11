---
title: Table.AutoFit
second_title: Aspose.Words لمراجع .NET API
description: Table طريقة. تغيير حجم الجدول والخلايا وفقًا لسلوك الاحتواء التلقائي المحدد.
type: docs
weight: 380
url: /ar/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

تغيير حجم الجدول والخلايا وفقًا لسلوك الاحتواء التلقائي المحدد.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| behavior | AutoFitBehavior | يحدد كيفية الملاءمة التلقائية للجدول. |

### ملاحظات

تحاكي هذه الطريقة الأوامر المتوفرة في قائمة الاحتواء التلقائي لجدول في Microsoft Word. الأوامر المتوفرة هي "الاحتواء التلقائي للمحتويات" و"الاحتواء التلقائي للنافذة" و"عرض العمود الثابت". في Microsoft Word ، تقوم هذه الأوامر بتعيين خصائص الجدول ذات الصلة ثم تحديث تخطيط الجدول ويقوم Aspose.Words بنفس الشيء بالنسبة لك.

### أمثلة

يوضح كيفية إنشاء جدول جديد أثناء تطبيق النمط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// يجب علينا إدراج صف واحد على الأقل قبل تعيين أي تنسيق للجدول.
builder.InsertCell();

// قم بتعيين نمط الجدول المستخدم بناءً على معرف النمط.
// لاحظ أنه ليست كل أنماط الجدول متاحة عند الحفظ بتنسيق .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// قم بتطبيق النمط جزئيًا على ميزات الجدول استنادًا إلى المسندات، ثم أنشئ الجدول.
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
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


