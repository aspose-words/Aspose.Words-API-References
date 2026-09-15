---
title: "Aspose::Words::Fields::FieldSeq فئة"
linktitle: "FieldSeq"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldSeq فئة. ينفّذ حقل SEQ. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 91000
url: /ar/cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


يُنفّذ الحقل SEQ. لتعلم المزيد، زر [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | يحصل أو يعيّن اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_InsertNextNumber](./get_insertnextnumber/)() | يحصل أو يعيّن ما إذا كان سيتم إدراج رقم التسلسل التالي للعنصر المحدد. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | يحصل أو يعيّن عددًا صحيحًا يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه. يُعيد -1 إذا كان العدد غير موجود. |
| [get_ResetNumber](./get_resetnumber/)() | يحصل أو يعيّن عددًا صحيحًا لإعادة تعيين رقم التسلسل إليه. يُعيد -1 إذا كان العدد غير موجود. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | يحصل أو يعيّن الاسم المخصص لسلسلة العناصر التي سيتم ترقيمها. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldSeq::get_BookmarkName](./get_bookmarkname/). |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/). |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

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


يعرض إنشاء الترقيم باستخدام حقول SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حقول SEQ تعرض عدًّا يزداد في كل حقل SEQ.
// هذه الحقول تحافظ أيضًا على عدّات منفصلة لكل تسلسل مسمى فريد
// مُحدَّد بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// أدرج حقل SEQ سيعرض القيمة الحالية للعدد لـ "MySequence",
// بعد استخدام الخاصية "ResetNumber" لتعيينه إلى 100.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// اعرض الرقم التالي في هذه السلسلة باستخدام حقل SEQ آخر.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// أدرج عنوانًا من المستوى 1.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// أدرج حقل SEQ آخر من نفس السلسلة وقم بتكوينه لإعادة تعيين العدد عند كل عنوان إلى 1.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// العنوان أعلاه هو عنوان من المستوى 1، لذا يتم إعادة تعيين عدد هذه السلسلة إلى 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// انتقل إلى الرقم التالي لهذه السلسلة.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```


يعرض كيفية دمج جدول المحتويات وحقول التسلسل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// يمكن لحقل TOC إنشاء إدخال في جدول محتوياته لكل حقل SEQ يُعثر عليه في المستند.
// كل إدخال يحتوي على الفقرة التي تحتوي على حقل SEQ،
// والرقم الصفحة التي يظهر فيها الحقل.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// قم بتكوين حقل TOC هذا ليحتوي على خاصية SequenceIdentifier بقيمة "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// قم بتكوين حقل TOC هذا ليلتقط فقط حقول SEQ التي تقع ضمن حدود إشارة مرجعية
// المسماة "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// حقول SEQ تعرض عدًّا يزداد في كل حقل SEQ.
// هذه الحقول تحافظ أيضًا على عدّات منفصلة لكل تسلسل مسمى فريد
// مُحدَّد بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// أدرج حقل SEQ يحتوي على معرف تسلسل يتطابق مع TOC's
// خاصية TableOfFiguresLabel. هذا الحقل لن ينشئ إدخالًا في TOC لأنه خارج
// حدود الإشارة المرجعية المحددة بواسطة "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// تطابق تسلسل حقل SEQ هذا خاصية "TableOfFiguresLabel" للـ TOC وهو ضمن حدود الإشارة المرجعية.
// الفقرة التي تحتوي على هذا الحقل ستظهر في TOC كإدخال.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// تسلسل حقل SEQ هذا لا يتطابق مع خاصية "TableOfFiguresLabel" للـ TOC،
// وهو ضمن حدود الإشارة المرجعية. فقرتها لن تظهر في TOC كإدخال.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// تطابق تسلسل حقل SEQ هذا خاصية "TableOfFiguresLabel" للـ TOC وهو ضمن حدود الإشارة المرجعية.
// هذا الحقل يشير أيضًا إلى إشارة مرجعية أخرى. محتويات تلك الإشارة المرجعية ستظهر في إدخال TOC لهذا الحقل SEQ.
// حقل SEQ نفسه لن يعرض محتويات تلك الإشارة المرجعية.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// أنشئ إشارة مرجعية بمحتويات ستظهر في إدخال TOC بسبب إشارة حقل SEQ أعلاه إليها.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
