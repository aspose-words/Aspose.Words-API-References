---
title: get_ImlRenderingMode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining how ink (InkML) objects are rendered.
type: docs
weight: 118
url: /cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


Gets or sets a value determining how ink (InkML) objects are rendered.

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## Remarks


The default value is [InkML](../../imlrenderingmode/).

This property is used when the document is exported to fixed page formats.

## Examples



Shows how to render Ink object. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Ink object.docx");

// Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
// If the rendering result is unsatisfactory,
// please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
auto saveOptions = MakeObject<ImageSaveOptions>(SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(ImlRenderingMode::InkML);

doc->Save(ArtifactsDir + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## See Also

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
