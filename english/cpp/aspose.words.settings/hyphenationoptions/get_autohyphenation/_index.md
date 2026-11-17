---
title: Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation method
linktitle: get_AutoHyphenation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation method. Gets or sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is false in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.settings/hyphenationoptions/get_autohyphenation/
---
## HyphenationOptions::get_AutoHyphenation method


Gets or sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is **false**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation() const
```


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

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
