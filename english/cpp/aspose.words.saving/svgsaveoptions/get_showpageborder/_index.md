---
title: get_ShowPageBorder
second_title: Aspose.Words for C++ API Reference
description: Controls whether a border is added to the outline of the page. Default is true.
type: docs
weight: 92
url: /cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions.get_ShowPageBorder method


Controls whether a border is added to the outline of the page. Default is **true**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
```


## Examples




Shows how to mimic the properties of images when converting a .docx document to .svg. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

// Configure the SvgSaveOptions object to save with no page borders or selectable text.
auto options = MakeObject<SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(ArtifactsDir + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

