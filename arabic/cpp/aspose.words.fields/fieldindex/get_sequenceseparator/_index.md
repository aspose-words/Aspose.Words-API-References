---
title: "Aspose::Words::Fields::FieldIndex::get_SequenceSeparator طريقة"
linktitle: "get_SequenceSeparator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldIndex::get_SequenceSeparator طريقة. يحصل أو يضبط تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.fields/fieldindex/get_sequenceseparator/
---
## FieldIndex::get_SequenceSeparator method


يحصل أو يعيّن تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_SequenceSeparator()
```


## أمثلة



يظهر كيفية تقسيم مستند إلى أجزاء عن طريق دمج حقول INDEX و SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء حقل INDEX سيعرض مدخلاً لكل حقل XE يُعثر عليه في المستند.
// سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
// إذا كان لحقل XE نفس القيمة في خاصية "Text" الخاصة به،
// سوف يقوم حقل INDEX بتجميعها في مدخل واحد.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// في خاصية SequenceName، قم بتسمية تسلسل حقل SEQ. كل إدخال في هذا الحقل INDEX سيعرض الآن أيضًا
// الرقم الذي يكون فيه عدّ التسلسل عند موقع حقل XE الذي أنشأ هذا الإدخال.
index->set_SequenceName(u"MySequence");

// حدد النص الذي سيحيط بأرقام التسلسل والصفحات لتوضيح معناها للمستخدم.
// سيعرض إدخال تم إنشاؤه بهذه التكوين شيئًا مثل "MySequence at 1 on page 1" عند رقم صفحته.
// لا يمكن أن يكون PageNumberSeparator و SequenceSeparator أطول من 15 حرفًا.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// حقول SEQ تعرض عدًّا يزداد في كل حقل SEQ.
// هذه الحقول تحافظ أيضًا على عدّات منفصلة لكل تسلسل مسمى فريد
// مُحدَّد بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// أدرج حقل SEQ الذي ينقل تسلسل "MySequence" إلى 1.
// هذا الحقل لا يختلف عن نص المستند العادي. لن يظهر في جدول محتويات حقل INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// أدرج حقل XE الذي سيُنشئ إدخالًا في حقل INDEX.
// نظرًا لأن "MySequence" في 1 وهذا الحقل XE في الصفحة 2، جنبًا إلى جنب مع الفواصل المخصصة التي عرّفناها أعلاه،
// سوف يعرض إدخال INDEX لهذا الحقل "Cat" على الجانب الأيسر، و"MySequence at 1 on page 2" على الجانب الأيمن.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// أدرج فاصل صفحة واستخدم حقول SEQ لتقدم "MySequence" إلى 3.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// أدرج حقل XE مع خاصية Text نفسها كما في السابق.
// سوف يجمع إدخال INDEX حقول XE ذات القيم المتطابقة في خاصية "Text".
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
// نظرًا لأننا في الصفحة 2 مع "MySequence" عند 3، سيتم إلحاق ", 3 on page 3" بنفس إدخال INDEX كما سبق.
// سوف يعرض الجزء المتعلق برقم الصفحة من إدخال INDEX ذلك الآن "MySequence at 1 on page 2, 3 on page 3".
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// أدرج حقل XE بقيمة خاصية Text جديدة وفريدة.
// سيضيف هذا إدخالًا جديدًا، مع MySequence عند 3 في الصفحة 4.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## انظر أيضًا

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
