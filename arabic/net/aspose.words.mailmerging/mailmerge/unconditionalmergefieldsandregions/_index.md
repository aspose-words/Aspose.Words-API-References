---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية UnconditionalMergeFieldsAndRegions في MailMerge على تعزيز أتمتة المستندات من خلال دمج الحقول والمناطق دون حدود شرطية.
type: docs
weight: 140
url: /ar/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

يحصل على قيمة أو يعينها تشير إلى ما إذا كانت حقول الدمج ومناطق الدمج مدمجة بغض النظر عن حالة حقل IF الرئيسي.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

## أمثلة

يوضح كيفية دمج الحقول أو المناطق بغض النظر عن حالة حقل IF الأصلي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل MERGEFIELD متداخلاً داخل حقل IF.
// نظرًا لأن عبارة الحقل IF خاطئة، فلن يتم عرض نتيجة MERGEFIELD.
// لن يستقبل MERGEFIELD أيضًا أي بيانات أثناء دمج البريد.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// إذا قمنا بتعيين علامة "UnconditionalMergeFieldsAndRegions" إلى "true"،
// سوف يقوم دمج البريد الخاص بنا بإدراج البيانات في الحقول غير المعروضة مثل حقل MERGEFIELD الخاص بنا بالإضافة إلى جميع الحقول الأخرى.
// إذا قمنا بتعيين علامة "UnconditionalMergeFieldsAndRegions" إلى "false"،
// لن يقوم دمج البريد الخاص بنا بإدراج البيانات في MERGEFIELDs المخفية بواسطة حقول IF التي تحتوي على عبارات خاطئة.
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
