---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words لـ .NET
description: حسّن دمج البريد باستخدام خاصية CleanupParagraphsWithPunctuationMarks. تحكّم في إزالة الفقرات الفارغة لمستندات أكثر دقةً واحترافية.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

يحصل على قيمة أو يعينها تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذاRemoveEmptyParagraphs تم تحديد الخيار.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي` .

فيما يلي القائمة الكاملة لعلامات الترقيم القابلة للتنظيف:

* !
* ،
* .
* :
* ؛
* ؟
* ¡
* ؟

## أمثلة

يوضح كيفية إزالة الفقرات التي تحتوي على علامات الترقيم بعد عملية دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// قم بتكوين خاصية "CleanupOptions" لإزالة أي فقرات فارغة قد ينشئها دمج البريد هذا.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// سيؤدي تعيين الخاصية "CleanupParagraphsWithPunctuationMarks" إلى "true" إلى حساب الفقرات أيضًا
// مع علامات الترقيم فارغة وسوف يتم تنفيذ عملية دمج البريد لإزالتها أيضًا.
// تعيين الخاصية "CleanupParagraphsWithPunctuationMarks" إلى "false"
// سوف يقوم بإزالة الفقرات الفارغة، ولكن ليس الفقرات التي تحتوي على علامات الترقيم.
// هذه قائمة علامات الترقيم التي تخص هذه الخاصية: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
