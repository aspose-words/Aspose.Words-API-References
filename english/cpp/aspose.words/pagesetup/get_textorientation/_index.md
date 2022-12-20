---
title: get_TextOrientation
second_title: Aspose.Words for C++ API Reference
description: Allows to specify TextOrientation for the whole page. Default value is Horizontal
type: docs
weight: 573
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
auto doc = MakeObject<Document>();

auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
// to the right so that all left-to-right text now goes top-to-bottom.
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(TextOrientation::Upward);

doc->Save(ArtifactsDir + u"PageSetup.SetTextOrientation.docx");
```

## See Also

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
