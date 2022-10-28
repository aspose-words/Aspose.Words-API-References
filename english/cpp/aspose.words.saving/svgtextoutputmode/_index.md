---
title: SvgTextOutputMode
second_title: Aspose.Words for C++ API Reference
description: 
type: docs
weight: 1041
url: /cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum




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

