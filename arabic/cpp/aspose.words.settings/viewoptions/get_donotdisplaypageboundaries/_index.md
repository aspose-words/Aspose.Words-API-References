---
title: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries طريقة"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries طريقة. يوقف عرض المسافة بين أعلى النص والحافة العلوية للصفحة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


يقوم بإيقاف عرض المسافة بين أعلى النص وحافة الصفحة العليا.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## أمثلة



يظهر كيفية إخفاء الفراغ العمودي والرؤوس/التذييلات في خيارات العرض.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج محتوى يمتد عبر 3 صفحات.
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// إدراج رأس وتذييل.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// يحتوي هذا المستند على كمية صغيرة من المحتوى تشغل مساحة تعادل بضع صفحات كاملة.
// اضبط علم "DoNotDisplayPageBoundaries" إلى "true" لجعل إصدارات Microsoft Word القديمة تتجاهل الرؤوس،
// التذييلات، والكثير من الفراغ العمودي عند عرض مستندنا.
// اضبط علم "DoNotDisplayPageBoundaries" إلى "false" لجعل إصدارات Microsoft Word القديمة
// تعرض مستندنا بشكل طبيعي.
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## انظر أيضًا

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
