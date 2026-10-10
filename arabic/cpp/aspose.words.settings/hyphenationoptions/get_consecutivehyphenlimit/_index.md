---
title: "طريقة Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit. يحصل أو يضبط الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات. القيمة الافتراضية لهذه الخاصية هي 0 في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


يحصل أو يضبط الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات. القيمة الافتراضية لهذه الخاصية هي 0.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## ملاحظات


إذا تم تعيين قيمة هذه الخاصية إلى 0، يمكن لأي عدد من الأسطر المتتالية أن ينتهي بشرطات.

هذه الخاصية لا تأثير لها عند الحفظ إلى صيغ الصفحات الثابتة مثل PDF.

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
