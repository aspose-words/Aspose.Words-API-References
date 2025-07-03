---
title: Aspose::Words::Settings::HyphenationOptions class
linktitle: HyphenationOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::HyphenationOptions class. Allows to configure document hyphenation options. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


Allows to configure document hyphenation options. To learn more, visit the [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/) documentation article.

```cpp
class HyphenationOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | Gets or sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | Gets or sets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | Gets or sets value determining whether words written in all capital letters are hyphenated. Default value for this property is **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | Gets or sets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. Default value for this property is 360 (0.25 inch). |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | Setter for [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | Setter for [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | Setter for [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | Setter for [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

## Examples



Shows how to configure automatic hyphenation. 
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

## See Also

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
