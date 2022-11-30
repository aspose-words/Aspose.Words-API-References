---
title: get_ShowHiddenText
second_title: Aspose.Words for C++ API Reference
description: Gets or sets indication of whether hidden text in the document is rendered. Default is False.
type: docs
weight: 79
url: /cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


Gets or sets indication of whether hidden text in the document is rendered. Default is False.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## Examples



Shows how to hide text in a rendered output document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert hidden text, then specify whether we wish to omit it from a rendered document.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(ArtifactsDir + u"Document.LayoutOptionsHiddenText.pdf");
```

## See Also

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words](../../../)
