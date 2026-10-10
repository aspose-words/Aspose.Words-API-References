---
title: "طريقة Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation"
linktitle: "get_AutoHyphenation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation. يحصل أو يضبط القيمة التي تحدد ما إذا كان التقسيم التلقائي مفعلاً للمستند. القيمة الافتراضية لهذه الخاصية هي false في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.settings/hyphenationoptions/get_autohyphenation/
---
## HyphenationOptions::get_AutoHyphenation method


يحصل أو يضبط القيمة التي تحدد ما إذا كان التجزئة التلقائية مفعلة للمستند. القيمة الافتراضية لهذه الخاصية هي **false**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation() const
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
