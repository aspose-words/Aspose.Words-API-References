---
title: "طريقة Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel"
linktitle: "get_ResetHeadingLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel. يحصل على أو يضبط عددًا صحيحًا يمثل مستوى عنوان لإعادة تعيين رقم التسلسل إليه. تُرجع -1 إذا كان العدد غير موجود في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fields/fieldseq/get_resetheadinglevel/
---
## FieldSeq::get_ResetHeadingLevel method


يحصل أو يعيّن عددًا صحيحًا يمثل مستوى العنوان لإعادة تعيين رقم التسلسل إليه. يُعيد -1 إذا كان العدد غير موجود.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel()
```


## أمثلة



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
