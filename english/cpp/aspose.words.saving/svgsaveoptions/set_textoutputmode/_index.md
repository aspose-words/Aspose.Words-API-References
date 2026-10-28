---
title: Aspose::Words::Saving::SvgSaveOptions::set_TextOutputMode method
linktitle: set_TextOutputMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::set_TextOutputMode method. Sets a value determining how text should be rendered in SVG in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.saving/svgsaveoptions/set_textoutputmode/
---
## SvgSaveOptions::set_TextOutputMode method


Sets a value determining how text should be rendered in SVG.

```cpp
void Aspose::Words::Saving::SvgSaveOptions::set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode value)
```

## Remarks


Use this property to get or set the mode of how text inside a document should be rendered when saving in SVG format.

The default value is [UseTargetMachineFonts](../../svgtextoutputmode/).
## Examples


Shows how to mimic the properties of images when converting a .docx document to .svg.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));

// Configure the SvgSaveOptions object to save with no page borders or selectable text.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```
## See Also

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
