---
title: "Aspose::Words::PageSetup::get_BorderSurroundsHeader method"
linktitle: "get_BorderSurroundsHeader"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup::get_BorderSurroundsHeader method. يحدد ما إذا كان حد الصفحة يتضمن أو يستثني الترويسة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/pagesetup/get_bordersurroundsheader/
---
## PageSetup::get_BorderSurroundsHeader method


يحدد ما إذا كان حد الصفحة يشمل أو يستثني الرأس.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsHeader()
```


## أمثلة



يوضح كيفية تطبيق حد على الصفحة والرأس/التذييل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// أدرج حدًا مزدوجًا أزرق.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// كائن PageSetup في القسم يحتوي على علمي "BorderSurroundsHeader" و "BorderSurroundsFooter" اللذين يحددان
// ما إذا كان حد الصفحة يحيط بنص الجسم الرئيسي، كما يتضمن الرأس أو التذييل على التوالي.
// اضبط علم "BorderSurroundsHeader" إلى "true" لتحيط الرأس بحدنا،
// ثم اضبط علم "BorderSurroundsFooter" لترك التذييل خارج الحد.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
