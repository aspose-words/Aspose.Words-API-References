---
title: "طريقة Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier"
linktitle: "get_SequenceIdentifier"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier. يحصل على أو يضبط الاسم المخصص لسلسلة العناصر التي سيتم ترقيمها في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.fields/fieldseq/get_sequenceidentifier/
---
## FieldSeq::get_SequenceIdentifier method


يحصل أو يعيّن الاسم المخصص لسلسلة العناصر التي سيتم ترقيمها.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier()
```


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

## انظر أيضًا

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
