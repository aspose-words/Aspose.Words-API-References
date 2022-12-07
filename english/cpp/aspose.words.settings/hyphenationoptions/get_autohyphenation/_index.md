---
title: get_AutoHyphenation
second_title: Aspose.Words for C++ API Reference
description: Gets or sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is false.
type: docs
weight: 27
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
* Library [Aspose.Words](../../../)
