---
title: "Aspose::Words::LowCode::MailMergeOptions فئة"
linktitle: "خيارات دمج البريد"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::LowCode::MailMergeOptions فئة. تمثل خيارات لوظيفة دمج البريد في C++."
type: docs
weight: 750
url: /ar/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


يمثل خيارات وظيفة دمج البريد.

```cpp
class MailMergeOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | يحصل على مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | يحصل أو يعيّن قيمة تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تُعتبر فارغة ويجب إزالتها إذا تم تحديد خيار [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/). |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | يحصل على قيمة تشير إلى ما إذا كان يجب دمج جميع مناطق دمج البريد في المستند التي تحمل اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أم فقط الأولى. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | يحصل على قيمة تشير إلى ما إذا كانت الحقول في المستند بالكامل تُحدَّث أثناء تنفيذ دمج البريد مع المناطق. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | يحصل على قيمة تشير إلى ما إذا كان يجب الحفاظ على العلامات "mustache" غير المستخدمة. |
| [get_RegionEndTag](./get_regionendtag/)() const | يحصل على علامة نهاية منطقة دمج البريد. |
| [get_RegionStartTag](./get_regionstarttag/)() const | يحصل على علامة بداية منطقة دمج البريد. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | يحصل على قيمة تشير إلى ما إذا كانت القوائم تُعاد بدءها في كل قسم بعد تنفيذ دمج البريد. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | يحصل على قيمة تشير إلى ما إذا كان بدء القسم من القسم الأول للمستند ونسخه للصفوف اللاحقة لمصدر البيانات يُحتفظ به أثناء دمج البريد أو يُحدَّث وفق سلوك MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | يحصل على قيمة تشير إلى ما إذا كانت المسافات الفارغة في البداية والنهاية تُقَص من قيم دمج البريد. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | يحصل على قيمة تشير إلى ما إذا كانت حقول الدمج ومناطق الدمج تُدمج بغض النظر عن شرط حقل IF الأب. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | عند **true**، يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم تنفيذ دمج البريد في بعض الأنواع الأخرى من الحقول وأيضًا في وسوم "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | يحصل على قيمة تشير إلى ما إذا كان الفقرة الكاملة التي تحتوي على حقل **TableStart** أو **TableEnd** أو النطاق المحدد بين حقلي **TableStart** و **TableEnd** يجب أن تُدرج في منطقة دمج البريد. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | يضبط مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | دالة ضبط لـ [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | يضبط قيمة تشير إلى ما إذا كان يجب دمج جميع مناطق دمج البريد في المستند التي تحمل اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أو فقط الأولى. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | يضبط قيمة تشير إلى ما إذا كانت الحقول في المستند بالكامل تُحدَّث أثناء تنفيذ دمج البريد مع المناطق. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | يضبط قيمة تشير إلى ما إذا كان يجب الحفاظ على وسوم "mustache" غير المستخدمة. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | يضبط وسم نهاية منطقة دمج البريد. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | يضبط وسم بداية منطقة دمج البريد. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | يضبط قيمة تشير إلى ما إذا كانت القوائم تُعاد بدءها في كل قسم بعد تنفيذ دمج البريد. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | يضبط قيمة تشير إلى ما إذا كان بدء القسم من القسم الأول للمستند ونسخه للصفوف اللاحقة لمصدر البيانات يُحتفظ به أثناء دمج البريد أو يُحدَّث وفق سلوك MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | يضبط قيمة تشير إلى ما إذا كانت المسافات الفارغة في البداية والنهاية تُقَص من قيم دمج البريد. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | يضبط قيمة تشير إلى ما إذا كانت حقول الدمج ومناطق الدمج تُدمج بغض النظر عن شرط حقل IF الأب. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | دالة ضبط لـ [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | يضبط قيمة تشير إلى ما إذا كان الفقرة الكاملة التي تحتوي على حقل **TableStart** أو **TableEnd** أو النطاق المحدد بين حقلي **TableStart** و **TableEnd** يجب أن تُدرج في منطقة دمج البريد. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
