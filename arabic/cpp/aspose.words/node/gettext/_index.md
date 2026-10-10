---
title: "طريقة Aspose::Words::Node::GetText"
linktitle: "GetText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Node::GetText. يحصل على النص لهذه العقدة وجميع أبنائها في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words/node/gettext/
---
## Node::GetText method


يحصل على نص هذا العقد وجميع أطفاله.

```cpp
virtual System::String Aspose::Words::Node::GetText()
```

## ملاحظات


السلسلة المرتجعة تشمل جميع أحرف التحكم والأحرف الخاصة كما هو موضح في [ControlChar](../../controlchar/).

## أمثلة



يعرض كيفية استخدام الأحرف التحكمية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج فقرات بنص باستخدام DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// تحويل المستند إلى صيغة نصية يكشف أن الأحرف التحكمية
// تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// عند تحويل مستند إلى صيغة سلسلة،
// يمكننا حذف بعض الأحرف التحكمية باستخدام طريقة Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```


يوضح كيفية إنشاء مستند Aspose.Words يدويًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// يحتوي مستند فارغ على قسم واحد، جسم واحد وفقرة واحدة.
// استدعِ طريقة "RemoveAllChildren" لإزالة جميع تلك العقد،
// وانتهي إلى عقدة مستند بدون أي أبناء.
doc->RemoveAllChildren();

// ليس لهذا المستند الآن أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تعديلها، سنحتاج إلى إعادة ملء مجموعة العقد الخاصة بها.
// أولاً، أنشئ قسمًا جديدًا، ثم أضفه كطفل إلى عقدة المستند الجذرية.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// حدد بعض خصائص إعداد الصفحة للقسم.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// يحتاج القسم إلى جسم، سيحتوي ويعرض جميع محتوياته
// على الصفحة بين رأس وتذييل القسم.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// أنشئ فقرة، واضبط بعض خصائص التنسيق، ثم أضفها كعنصر فرعي إلى الجسم.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// أخيرًا، أضف بعض المحتوى لإنشاء المستند. أنشئ عنصر Run،
// اضبط مظهره ومحتوياته، ثم أضفه كعنصر فرعي إلى الفقرة.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## انظر أيضًا

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
