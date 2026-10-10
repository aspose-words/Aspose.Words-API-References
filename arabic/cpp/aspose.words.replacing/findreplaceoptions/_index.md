---
title: "فئة Aspose::Words::Replacing::FindReplaceOptions"
linktitle: "FindReplaceOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Replacing::FindReplaceOptions. تحدد الخيارات لعمليات البحث/الاستبدال. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


يحدد خيارات عمليات البحث/الاستبدال. لمعرفة المزيد، زر مقالة الوثائق [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class FindReplaceOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | ينشئ مثيلًا جديدًا من الفئة [FindReplaceOptions](./) بالإعدادات الافتراضية. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | ينشئ مثيلًا جديدًا من الفئة [FindReplaceOptions](./) بالاتجاه المحدد. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | ينشئ مثيلًا جديدًا من الفئة [FindReplaceOptions](./) بدالة الاستبدال المحددة. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | ينشئ مثيلًا جديدًا من الفئة [FindReplaceOptions](./) بالاتجاه المحدد ودالة الاستبدال. |
| [get_ApplyFont](./get_applyfont/)() const | تنسيق النص المطبق على المحتوى الجديد. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | تنسيق [Paragraph](../../aspose.words/paragraph/) المطبق على المحتوى الجديد. |
| [get_Direction](./get_direction/)() const | يحدد الاتجاه للاستبدال. القيمة الافتراضية هي [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True يدل على أن oldValue يجب أن تكون كلمة مستقلة. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الحذف. القيمة الافتراضية هي **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل رموز الحقول. القيمة الافتراضية هي **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل الحقول. القيمة الافتراضية هي **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الحواشي السفلية. القيمة الافتراضية هي **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل مراجعات الإدراج. القيمة الافتراضية هي **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل النص داخل OfficeMath/>. القيمة الافتراضية هي **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الأشكال داخل النص. القيمة الافتراضية هي **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل محتوى [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). القيمة الافتراضية هي **false**. |
| [get_LegacyMode](./get_legacymode/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى أن خوارزمية البحث/الاستبدال القديمة تُستخدم. |
| [get_MatchCase](./get_matchcase/)() const | True يدل على مقارنة حساسة لحالة الأحرف، false يدل على مقارنة غير حساسة لحالة الأحرف. |
| [get_ReplacementFormat](./get_replacementformat/)() const | يحدد تنسيق الاستبدال. القيمة الافتراضية هي [النص](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | الطريقة المعرفة من قبل المستخدم والتي يتم استدعاؤها قبل كل حدوث استبدال. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان مسموحًا باستبدال فاصل الفقرة عندما لا يوجد فقرة شقيقة تالٍ. القيمة الافتراضية هي **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | صحيح يشير إلى أن البحث النصي يتم بشكل متسلسل من الأعلى إلى الأسفل مع مراعاة صناديق النص. القيمة الافتراضية هي **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب التعرف على الاستبدالات واستخدامها داخل أنماط الاستبدال. القيمة الافتراضية هي **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | يحدد الاتجاه للاستبدال. القيمة الافتراضية هي [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/). |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/). |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/). |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/). |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/). |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/). |
| [set_LegacyMode](./set_legacymode/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/). |
| [set_MatchCase](./set_matchcase/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/). |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | يحدد تنسيق الاستبدال. القيمة الافتراضية هي [النص](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | الطريقة المعرفة من قبل المستخدم والتي يتم استدعاؤها قبل كل حدوث استبدال. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/). |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | صحيح يشير إلى أن البحث النصي يتم بشكل متسلسل من الأعلى إلى الأسفل مع مراعاة صناديق النص. القيمة الافتراضية هي **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | محدد القيمة لـ [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية تبديل حساسية حالة الأحرف عند تنفيذ عملية البحث والاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// عيّن علم "MatchCase" إلى "true" لتطبيق حساسية حالة الأحرف أثناء البحث عن السلاسل لاستبدالها.
// عيّن علم "MatchCase" إلى "false" لتجاهل حالة الأحرف أثناء البحث عن النص لاستبداله.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


يوضح كيفية تبديل عمليات البحث والاستبدال التي تقتصر على الكلمات المستقلة فقط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// عيّن علم "FindWholeWordsOnly" إلى "true" لاستبدال النص الموجود إذا لم يكن جزءًا من كلمة أخرى.
// عيّن علم "FindWholeWordsOnly" إلى "false" لاستبدال كل النص بغض النظر عن محيطه.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## انظر أيضًا

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
