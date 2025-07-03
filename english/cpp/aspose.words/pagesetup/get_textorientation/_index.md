---
title: Aspose::Words::PageSetup::get_TextOrientation method
linktitle: get_TextOrientation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_TextOrientation method. Allows to specify TextOrientation for the whole page. Default value is Horizontal in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


Allows to specify [TextOrientation](./) for the whole page. Default value is [Horizontal](../../textorientation/)

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## Examples



Shows how to set text orientation. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
// to the right so that all left-to-right text now goes top-to-bottom.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## See Also

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
