---
title: "طريقة Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone"
linktitle: "get_HyphenationZone"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone. يحصل على أو يحدد المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا ترغب في تقطيع الكلمات فيها. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة) في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


يحصل أو يضبط المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا ترغب في تقسيم الكلمات داخلها. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة).

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
```


## أمثلة



يعرض كيفية تكوين التجزئة التلقائية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## انظر أيضًا

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
