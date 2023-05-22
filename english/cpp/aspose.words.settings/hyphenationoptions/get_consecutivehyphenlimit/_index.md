---
title: Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit method
linktitle: get_ConsecutiveHyphenLimit
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit method. Gets or sets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0 in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


Gets or sets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## Remarks


If value of this property is set to 0, any number of consecutive lines can end with hyphens.

The property does not have effect when saving to fixed page formats e.g. PDF.

## Examples



Shows how to configure automatic hyphenation. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") +
                 u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(ArtifactsDir + u"Document.HyphenationOptions.docx");
```

## See Also

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
