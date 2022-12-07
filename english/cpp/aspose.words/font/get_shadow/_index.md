---
title: get_Shadow
second_title: Aspose.Words for C++ API Reference
description: True if the font is formatted as shadowed.
type: docs
weight: 443
url: /cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


True if the font is formatted as shadowed.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## Examples



Shows how to create a run of text formatted with a shadow. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Set the Shadow flag to apply an offset shadow effect,
// making it look like the letters are floating above the page.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(ArtifactsDir + u"Font.Shadow.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
