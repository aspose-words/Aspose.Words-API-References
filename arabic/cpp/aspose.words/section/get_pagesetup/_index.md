---
title: "طريقة Aspose::Words::Section::get_PageSetup"
linktitle: "get_PageSetup"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Section::get_PageSetup. تُرجع كائنًا يمثل إعدادات الصفحة وخصائص القسم في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/section/get_pagesetup/
---
## Section::get_PageSetup method


يرجع كائناً يمثل إعدادات الصفحة وخصائص القسم.

```cpp
System::SharedPtr<Aspose::Words::PageSetup> Aspose::Words::Section::get_PageSetup()
```


## أمثلة



يظهر كيفية إنشاء حد على شكل شريط أزرق عريض في أعلى الصفحة الأولى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
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

* Class [PageSetup](../../pagesetup/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
