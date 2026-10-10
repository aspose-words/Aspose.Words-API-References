---
title: "Aspose::Words::ParagraphAlignment enum"
linktitle: "ParagraphAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphAlignment enum. يحدد محاذاة النص في الفقرة بلغة C++."
type: docs
weight: 110000
url: /ar/cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


يحدد محاذاة النص في الفقرة.

```cpp
enum class ParagraphAlignment
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| يسار | 0 | النص محاذى إلى اليسار. |
| وسط | 1 | النص مُوسَّط أفقياً. |
| يمين | 2 | النص محاذى إلى اليمين. |
| محاذاة | 3 | النص محاذى إلى اليسار واليمين. |
| موزع | 4 | النص موزَّع بالتساوي. |
| ArabicMediumKashida | 5 | العربية فقط. يتم تمديد طول الكاشدة للنص إلى طول متوسط يحدده المستهلك. |
| ArabicHighKashida | 7 | العربية فقط. يتم تمديد طول الكاشدة للنص إلى أقصى طول ممكن. |
| ArabicLowKashida | 8 | العربية فقط. يتم تمديد طول الكاشدة للنص إلى طول أطول قليلًا. |
| ThaiDistributed | 9 | التايلاندية فقط. النص مُضبط بمحاذاة كاملة مع تحسين للغة التايلاندية. |
| MathElementCenterAsGroup | 10 | العنصر الوحيد [Math](../../aspose.words.math/) في سطر، مُحاذى كـ 'مركّز كمجموعة'. |


## أمثلة



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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
