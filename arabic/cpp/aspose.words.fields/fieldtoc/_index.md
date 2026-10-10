---
title: "فئة Aspose::Words::Fields::FieldToc"
linktitle: "FieldToc"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldToc. تنفّذ حقل الفهرس. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 105000
url: /ar/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


يُنفّذ الحقل TOC. لتعلم المزيد، زر [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | يحصل على اسم العلامة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الجدول. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | يحصل أو يحدد اسم معرف التسلسل المستخدم عند إنشاء جدول الأشكال الذي لا يتضمن تسمية ورقم التسمية التوضيحية. |
| [get_CustomStyles](./get_customstyles/)() | يحصل على قائمة الأنماط غير الأنماط المدمجة للعناوين لتضمينها في جدول المحتويات. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_EntryIdentifier](./get_entryidentifier/)() | يحصل على سلسلة يجب أن تتطابق مع معرفات النوع لحقول TC التي يتم تضمينها. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | يحصل على نطاق المستويات لمدخلات جدول المحتويات التي سيتم تضمينها. |
| [get_EntrySeparator](./get_entryseparator/)() | يحصل على تسلسل من الأحرف التي تفصل بين المدخل ورقم صفحته. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | يحصل على نطاق مستويات العناوين لتضمينها. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | يحصل على ما إذا كان يجب إخفاء قائد التبويب وأرقام الصفحات في عرض تخطيط الويب. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | يحصل على ما إذا كان يجب جعل مدخلات جدول المحتويات روابط تشعبية. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | يحصل على نطاق المستويات لمدخلات جدول المحتويات التي يجب حذف أرقام الصفحات منها. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | يحصل أو يحدد معرف تسلسل يجب إضافة بادئة إلى رقم صفحة المدخل له. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | يحصل على ما إذا كان يجب الحفاظ على أحرف السطر الجديد داخل مدخلات الجدول. |
| [get_PreserveTabs](./get_preservetabs/)() | يحصل على ما إذا كان يجب الحفاظ على مدخلات التبويب داخل مدخلات الجدول. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | يحصل أو يعيّن تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | يحصل أو يحدد اسم معرف التسلسل المستخدم عند إنشاء جدول الأشكال. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | يحصل على ما إذا كان يجب استخدام مستوى مخطط الفقرة المطبق. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | يضبط اسم العلامة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الجدول. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | محدد لـ [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | يحدد قائمة الأنماط غير الأنماط المدمجة للعناوين لتضمينها في جدول المحتويات. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | يحدد سلسلة يجب أن تتطابق مع معرفات النوع لحقول TC التي يتم تضمينها. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | يحدد نطاق المستويات لمدخلات جدول المحتويات التي سيتم تضمينها. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | يحدد تسلسل من الأحرف التي تفصل بين المدخل ورقم صفحته. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | يحدد نطاق مستويات العناوين لتضمينها. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | يحدد ما إذا كان يجب إخفاء قائد التبويب وأرقام الصفحات في عرض تخطيط الويب. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | يحدد ما إذا كان يجب جعل مدخلات جدول المحتويات روابط تشعبية. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | يضبط نطاقًا من مستويات إدخالات جدول المحتويات التي يتم منها حذف أرقام الصفحات. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | يضبط ما إذا كان يجب الحفاظ على أحرف السطر الجديد داخل إدخالات الجدول. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | يضبط ما إذا كان يجب الحفاظ على علامات التبويب داخل إدخالات الجدول. |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | يضبط ما إذا كان يجب استخدام مستوى مخطط الفقرة المطبق. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
| [UpdatePageNumbers](./updatepagenumbers/)() | يقوم بتحديث أرقام الصفحات للعناصر في جدول المحتويات هذا. |

## أمثلة



يعرض كيفية تعبئة حقل TOC بإدخالات باستخدام حقول SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// يمكن لحقل TOC إنشاء إدخال في جدول محتوياته لكل حقل SEQ يُعثر عليه في المستند.
// كل إدخال يحتوي على الفقرة التي تشمل حقل SEQ ورقم الصفحة التي يظهر فيها الحقل.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// حقول SEQ تعرض عدًّا يزداد في كل حقل SEQ.
// هذه الحقول تحافظ أيضًا على عدّات منفصلة لكل تسلسل مسمى فريد
// مُحدَّد بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// استخدم خاصية "TableOfFiguresLabel" لتسمية تسلسل رئيسي لفهرس المحتويات.
// الآن، سيقوم هذا الفهرس بإنشاء إدخالات فقط من حقول SEQ التي تكون خاصية "SequenceIdentifier" فيها مضبوطة على "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// يمكننا تسمية تسلسل حقل SEQ آخر في خاصية "PrefixedSequenceIdentifier".
// حقول SEQ من هذا التسلسل المسبق لن تُنشئ إدخالات في الفهرس.
// كل إدخال في الفهرس يُنشأ من حقل SEQ لتسلسل رئيسي سيعرض الآن أيضًا العدد الذي
// التسلسل المسبق هو عليه حاليًا عند حقل SEQ للتسلسل الأساسي الذي أنشأ الإدخال.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// كل إدخال في الفهرس سيعرض عدد التسلسل المسبق مباشرةً إلى اليسار
// من رقم الصفحة التي يظهر فيها حقل SEQ للتسلسل الرئيسي.
// يمكننا تحديد فاصل مخصص سيظهر بين هذين الرقمين.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// هناك طريقتان لاستخدام حقول SEQ لملء هذا الفهرس.
// 1 -  إدراج حقل SEQ ينتمي إلى تسلسل الفهرس المسبق:
// هذا الحقل سيزيد عدد تسلسل SEQ الخاص بـ "PrefixSequence" بمقدار 1.
// نظرًا لأن هذا الحقل لا ينتمي إلى التسلسل الرئيسي المحدد
// بخاصية "TableOfFiguresLabel" للفهرس، لن يظهر كإدخال.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  إدراج حقل SEQ ينتمي إلى التسلسل الرئيسي للفهرس:
// هذا الحقل SEQ سيُنشئ إدخالًا في الفهرس.
// سيتضمن إدخال الفهرس الفقرة التي يوجد فيها حقل SEQ ورقم الصفحة التي يظهر فيها.
// سيعرض هذا الإدخال أيضًا العدد الذي يكون عليه التسلسل المسبق حاليًا،
// مفصولًا عن رقم الصفحة بالقيمة الموجودة في خاصية SeqenceSeparator للفهرس.
// عدد "PrefixSequence" هو 1، وحقل SEQ للتسلسل الرئيسي على الصفحة 2،
// والفاصل هو ">"، لذا سيعرض الإدخال "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// أدرج صفحة، قدِّم التسلسل المسبق بمقدار 2، وأدرج حقل SEQ لإنشاء إدخال في الفهرس بعد ذلك.
// التسلسل المسبق الآن هو 2، وحقل SEQ للتسلسل الرئيسي على الصفحة 3،
// لذلك سيعرض إدخال الفهرس "2>3" في عدد صفحته.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
