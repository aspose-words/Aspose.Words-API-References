---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words لـ .NET
description: MailMerge CleanupParagraphsWithPunctuationMarks ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذا كانتRemoveEmptyParagraphs تم تحديد الخيار في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذا كانتRemoveEmptyParagraphs تم تحديد الخيار.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`حقيقي` .

فيما يلي القائمة الكاملة لعلامات الترقيم القابلة للتنظيف:

* !
* ,
* .
* :
* ;
* ؟
* ¡
* ¿

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

// قم بتكوين خاصية "CleanupOptions" لإزالة أية فقرات فارغة قد يؤدي دمج المراسلات إلى إنشائها.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// تعيين الخاصية "CleanupParagraphsWithPcientationMarks" على "صحيح" سيؤدي أيضًا إلى حساب الفقرات
// مع وجود علامات ترقيم فارغة وستحصل على عملية دمج البريد لإزالتها أيضًا.
// ضبط الخاصية "CleanupParagraphsWithPcientationMarks" على "خطأ"
// سوف يزيل الفقرات الفارغة، ولكن ليس الفقرات التي تحتوي على علامات الترقيم.
// هذه قائمة بعلامات الترقيم التي تتعلق بهذه الخاصية: "!"، "،"، "."، ": "، ";"، "؟"، "¡"، "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
