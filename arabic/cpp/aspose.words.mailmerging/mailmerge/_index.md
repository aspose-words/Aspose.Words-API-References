---
title: "Aspose::Words::MailMerging::MailMerge class"
linktitle: "MailMerge"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::MailMerging::MailMerge class. يمثل وظيفة دمج البريد. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


يمثل وظيفة دمج البريد. لمعرفة المزيد، زر مقالة الوثائق [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMerge : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [DeleteFields](./deletefields/)() | يزيل الحقول المتعلقة بدمج البريد من المستند. |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | يُجري دمج بريد من مصدر بيانات مخصص. |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | يُجري عملية دمج بريد لسجل واحد. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | ينفّذ دمج بريد من مصدر بيانات مخصص مع مناطق دمج البريد. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | ينفّذ دمج بريد من مصدر بيانات مخصص مع مناطق دمج البريد. |
| [get_CleanupOptions](./get_cleanupoptions/)() const | يحصل على مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | يحصل أو يعيّن قيمة تشير إلى ما إذا كانت الفقرات التي تحتوي على علامات ترقيم تُعتبر فارغة ويجب إزالتها إذا تم تحديد خيار [RemoveEmptyParagraphs](../mailmergecleanupoptions/). |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | يحدث أثناء دمج البريد عندما يتم العثور على حقل دمج بريد في المستند. |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | يسمح بمعالجة أحداث معينة أثناء دمج البريد. |
| [get_MappedDataFields](./get_mappeddatafields/)() | يرجع مجموعة تمثل حقول البيانات المربّطة لعملية دمج البريد. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | يحصل على قيمة تشير إلى ما إذا كان يجب دمج جميع مناطق دمج البريد في المستند التي تحمل اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أم فقط الأولى. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | يحصل على قيمة تشير إلى ما إذا كانت الحقول في المستند بالكامل تُحدَّث أثناء تنفيذ دمج البريد مع المناطق. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | يحصل على قيمة تشير إلى ما إذا كان يجب الحفاظ على العلامات "mustache" غير المستخدمة. |
| [get_RegionEndTag](./get_regionendtag/)() const | يحصل على علامة نهاية منطقة دمج البريد. |
| [get_RegionStartTag](./get_regionstarttag/)() const | يحصل على علامة بداية منطقة دمج البريد. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | يحصل على قيمة تشير إلى ما إذا كانت القوائم تُعاد بدءها في كل قسم بعد تنفيذ دمج البريد. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | يحصل على قيمة تشير إلى ما إذا كان [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) للقسم الأول من المستند ونسخه للصفوف اللاحقة لمصدر البيانات يُحتفظ به أثناء دمج البريد أو يتم تحديثه وفق سلوك MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | يحصل على قيمة تشير إلى ما إذا كانت المسافات الفارغة في البداية والنهاية تُقَص من قيم دمج البريد. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | يحصل على قيمة تشير إلى ما إذا كانت حقول الدمج ومناطق الدمج تُدمج بغض النظر عن شرط حقل IF الأب. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | عند **true**، يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم تنفيذ دمج البريد في بعض الأنواع الأخرى من الحقول وأيضًا في وسوم "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | يحصل على قيمة تشير إلى ما إذا كان الفقرة الكاملة التي تحتوي على حقل **TableStart** أو **TableEnd** أو النطاق المحدد بين حقلي **TableStart** و **TableEnd** يجب أن تُدرج في منطقة دمج البريد. |
| [GetFieldNames](./getfieldnames/)() | يرجع مجموعة من أسماء حقول دمج البريد المتوفرة في المستند. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | يرجع مجموعة من أسماء حقول دمج البريد المتوفرة في المنطقة. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | يرجع مجموعة من أسماء حقول دمج البريد المتوفرة في المنطقة. |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | يرجع مجموعة من مناطق دمج البريد بالاسم المحدد. |
| [GetRegionsHierarchy](./getregionshierarchy/)() | يرجع هيكلًا كاملًا للمناطق (مع الحقول) المتوفرة في المستند. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | يضبط مجموعة من العلامات التي تحدد العناصر التي يجب إزالتها أثناء دمج البريد. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | مُعيّن لـ [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | يحدث أثناء دمج البريد عندما يتم العثور على حقل دمج بريد في المستند. |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | يسمح بمعالجة أحداث معينة أثناء دمج البريد. |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | يضبط قيمة تشير إلى ما إذا كان يجب دمج جميع مناطق دمج البريد في المستند التي تحمل اسم مصدر البيانات أثناء تنفيذ دمج البريد مع المناطق مقابل مصدر البيانات أو فقط الأولى. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | يضبط قيمة تشير إلى ما إذا كانت الحقول في المستند بالكامل تُحدَّث أثناء تنفيذ دمج البريد مع المناطق. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | يضبط قيمة تشير إلى ما إذا كان يجب الحفاظ على وسوم "mustache" غير المستخدمة. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | يضبط وسم نهاية منطقة دمج البريد. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | يضبط وسم بداية منطقة دمج البريد. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | يضبط قيمة تشير إلى ما إذا كانت القوائم تُعاد بدءها في كل قسم بعد تنفيذ دمج البريد. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | يعيّن قيمة تشير إلى ما إذا كان [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) للقسم الأول من المستند ونسخه للصفوف اللاحقة لمصدر البيانات يُحتفظ به أثناء دمج البريد أو يتم تحديثه وفق سلوك MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | يضبط قيمة تشير إلى ما إذا كانت المسافات الفارغة في البداية والنهاية تُقَص من قيم دمج البريد. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | يضبط قيمة تشير إلى ما إذا كانت حقول الدمج ومناطق الدمج تُدمج بغض النظر عن شرط حقل IF الأب. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | مُعيّن لـ [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | يضبط قيمة تشير إلى ما إذا كان الفقرة الكاملة التي تحتوي على حقل **TableStart** أو **TableEnd** أو النطاق المحدد بين حقلي **TableStart** و **TableEnd** يجب أن تُدرج في منطقة دمج البريد. |
| static [Type](./type/)() |  |
## ملاحظات


لكي تعمل عملية دمج البريد، يجب أن يحتوي المستند على حقول Word MERGEFIELD وربما حقول NEXT. أثناء عملية دمج البريد، يتم استبدال حقول الدمج في المستند بالقيم من مصدر البيانات الخاص بك.

هناك طريقتان مميزتان لاستخدام دمج البريد: مع مناطق دمج البريد وبدونها.

أبسط دمج بريد هو بدون مناطق وهو مشابه جدًا لكيفية عمل دمج البريد في Word. استخدم طرق **Execute** لدمج المعلومات من مصدر بيانات مثل **DataTable** أو **DataSet** أو مصفوفة من الكائنات إلى المستند الخاص بك. يقوم كائن [MailMerge](./) بمعالجة جميع سجلات مصدر البيانات ويُنسخ ويضيف محتوى المستند بالكامل لكل سجل.

لاحظ أنه عندما يواجه كائن [MailMerge](./) حقل NEXT، يختار السجل التالي في مصدر البيانات ويستمر في الدمج دون نسخ أي محتوى.

استخدم [ExecuteWithRegions()](../) وغيرها من التحميلات الزائدة لدمج المعلومات في مستند مع تعريف مناطق دمج البريد. يمكنك استخدامها كمصادر بيانات لهذه العملية.

تحتاج إلى استخدام مناطق دمج البريد إذا كنت تريد توسيع أجزاء داخل المستند ديناميكيًا. بدون مناطق دمج البريد سيتكرر المستند بالكامل لكل سجل من مصدر البيانات.

## انظر أيضًا

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
