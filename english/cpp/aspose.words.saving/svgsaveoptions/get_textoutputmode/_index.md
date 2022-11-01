---
title: get_TextOutputMode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining how text should be rendered in SVG.
type: docs
weight: 105
url: /cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions.get_TextOutputMode method


Gets or sets a value determining how text should be rendered in SVG.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```


Use this property to get or set the mode of how text inside a document should be rendered when saving in SVG format.

The default value is **UseTargetMachineFonts**.

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

