---
title: Aspose::Words::Saving::SvgTextOutputMode enum
linktitle: SvgTextOutputMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgTextOutputMode enum. Allows to specify how text inside a document should be rendered when saving in SVG format in C++.'
type: docs
weight: 83000
url: /cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


Allows to specify how text inside a document should be rendered when saving in SVG format.

```cpp
enum class SvgTextOutputMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| UseSvgFonts | 0 | SVG fonts are used to render text. Note, not all browsers support SVG fonts. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) installed on the target machine are used to render text. Note, if some of fonts used in the document are not available on the target machine, document can look differently. |
| UsePlacedGlyphs | 2 | Text is rendered using curves. Note, text selection will not work if you use this option. |


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

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
