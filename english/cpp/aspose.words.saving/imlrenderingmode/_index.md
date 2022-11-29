---
title: ImlRenderingMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how ink (InkML) objects are rendered to fixed page formats.
type: docs
weight: 846
url: /cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


Specifies how ink (InkML) objects are rendered to fixed page formats.

```cpp
enum class ImlRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Fallback | 0 | If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. |
| InkML | 1 | Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. This is the default mode. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
