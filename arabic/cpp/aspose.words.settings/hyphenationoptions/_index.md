---
title: "Aspose::Words::Settings::HyphenationOptions class"
linktitle: "HyphenationOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::HyphenationOptions class. يسمح بتكوين خيارات تجزئة الكلمات في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


يسمح بتكوين خيارات تجزئة الكلمات في المستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class HyphenationOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | يحصل أو يضبط القيمة التي تحدد ما إذا كان التجزئة التلقائية مفعلة للمستند. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | يحصل أو يضبط الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بشرطات. القيمة الافتراضية لهذه الخاصية هي 0. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | يحصل أو يضبط القيمة التي تحدد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة بالكامل تُقسم بشرطات. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | يحصل أو يضبط المسافة بوحدة 1/20 من النقطة من الهامش الأيمن التي لا ترغب في تقسيم الكلمات داخلها. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة). |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | مُعيّن لـ [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | مُعيّن لـ [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | مُعيّن لـ [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | مُعيّن لـ [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
