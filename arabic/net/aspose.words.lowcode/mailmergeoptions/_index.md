---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.MailMergeOptions لحلول دمج بريد سلسة وبسيطة. عزّز أتمتة مستنداتك بميزات قابلة للتخصيص!
type: docs
weight: 4260
url: /ar/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

يمثل خيارات لوظيفة دمج البريد.

```csharp
public class MailMergeOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | يحصل على مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد أو يعينها. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تعتبر فارغة ويجب إزالتها إذاRemoveEmptyParagraphs تم تحديد الخيار. |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى ما إذا كان يجب دمج جميع مناطق دمج البريد للمستندات التي تحمل اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أو المنطقة الأولى فقط. |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت الحقول في المستند بأكمله يتم تحديثها أثناء تنفيذ دمج البريد مع المناطق. |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | يحصل على قيمة تشير إلى ما إذا كان يجب الحفاظ على علامات "الشارب" غير المستخدمة أو تعيينها. |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | يحصل على علامة نهاية منطقة دمج البريد أو يعينها. |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | يحصل على علامة بدء منطقة دمج البريد أو يعينها. |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم إعادة تشغيل القوائم في كل قسم بعد تنفيذ دمج البريد. |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى ما إذا كان يتم الاحتفاظ ببداية قسم المستند الأول ونسخه لصفوف مصدر البيانات اللاحقة أثناء دمج البريد أو تحديثها وفقًا لسلوك MS Word. |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت المسافات البيضاء النهائية والبادئة يتم اقتصاصها من قيم دمج البريد. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى ما إذا كانت حقول الدمج ومناطق الدمج مدمجة بغض النظر عن حالة حقل IF الرئيسي. |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | عندما`حقيقي` , يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم تنفيذ دمج البريد في بعض الأنواع الأخرى من الحقول و أيضًا في علامات "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت الفقرة بأكملها تحتوي على**بدء تشغيل الجدول** أو**نهاية الجدول** field أو نطاق معين بين**بدء تشغيل الجدول** و**نهاية الجدول** يجب تضمين الحقول في منطقة دمج البريد. |

## أمثلة

يوضح كيفية إجراء عملية دمج البريد لسجل واحد.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
