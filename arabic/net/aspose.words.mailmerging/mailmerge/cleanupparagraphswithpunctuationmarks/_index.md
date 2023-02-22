---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words لمراجع .NET API
description: MailMerge ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذا كانRemoveEmptyParagraphs تم تحديد الخيار .
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذا كانRemoveEmptyParagraphs تم تحديد الخيار .

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`حقيقي` .

إليك القائمة الكاملة لعلامات الترقيم القابلة للتنظيف:

* !
* و
* .
* :
* ؛
* ؟
* ¡
* ¿

### أمثلة

يوضح كيفية إزالة الفقرات بعلامات الترقيم بعد عملية دمج المراسلات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// تكوين خاصية "CleanupOptions" لإزالة أية فقرات فارغة قد ينشئها دمج المراسلات هذا.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// سيؤدي تعيين خاصية "CleanupParagraphsWithPunctuationMarks" على "true" إلى حساب الفقرات أيضًا
// بعلامات الترقيم فارغة وسيحصل على عملية دمج المراسلات لإزالتها أيضًا.
// تعيين خاصية "CleanupParagraphsWithPunctuationMarks" على "false"
// سيزيل الفقرات الفارغة ، لكن ليس تلك التي تحتوي على علامات ترقيم.
// هذه قائمة بعلامات الترقيم التي تخص هذه الخاصية: "!"، "،"، "."، ":"، ";"، "؟"، "¡"، "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


