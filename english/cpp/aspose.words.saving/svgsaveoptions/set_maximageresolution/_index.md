---
title: Aspose::Words::Saving::SvgSaveOptions::set_MaxImageResolution method
linktitle: set_MaxImageResolution
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::set_MaxImageResolution method. Sets a value in pixels per inch that limits resolution of exported raster images. Default value is zero in C++.'
type: docs
weight: 14500
url: /cpp/aspose.words.saving/svgsaveoptions/set_maximageresolution/
---
## SvgSaveOptions::set_MaxImageResolution method


Sets a value in pixels per inch that limits resolution of exported raster images. Default value is zero.

```cpp
void Aspose::Words::Saving::SvgSaveOptions::set_MaxImageResolution(int32_t value)
```

## Remarks


 If the value of this property is non-zero, it limits resolution of exported raster images. That is, higher-resolution images are resampled down to the limit and lower-resolution images are exported as is. 

 If the value of this property is zero, all raster images are exported without resampling. 
## Examples


Shows how to set limit for image resolution.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```
## See Also

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
