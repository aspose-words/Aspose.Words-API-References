---
title: Aspose::Words::Saving::SvgSaveOptions::set_FitToViewPort method
linktitle: set_FitToViewPort
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::set_FitToViewPort method. Specifies if the output SVG should fill the available viewport area (browser window or container). When set to true width and height of output SVG are set to 100%. The default value is false in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.saving/svgsaveoptions/set_fittoviewport/
---
## SvgSaveOptions::set_FitToViewPort method


Specifies if the output SVG should fill the available viewport area (browser window or container). When set to **true** width and height of output SVG are set to 100%. 
The default value is **false**.

```cpp
void Aspose::Words::Saving::SvgSaveOptions::set_FitToViewPort(bool value)
```

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
