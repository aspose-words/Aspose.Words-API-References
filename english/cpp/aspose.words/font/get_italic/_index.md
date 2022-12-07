---
title: get_Italic
second_title: Aspose.Words for C++ API Reference
description: True if the font is formatted as italic.
type: docs
weight: 222
url: /cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


True if the font is formatted as italic.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## Examples



Shows how to write italicized text using a document builder. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(ArtifactsDir + u"Font.Italic.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
