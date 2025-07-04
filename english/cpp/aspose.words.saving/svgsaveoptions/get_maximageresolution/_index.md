---
title: Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution method
linktitle: get_MaxImageResolution
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution method. Gets or sets a value in pixels per inch that limits resolution of exported raster images. Default value is zero in C++.'
type: docs
weight: 4500
url: /cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


Gets or sets a value in pixels per inch that limits resolution of exported raster images. Default value is zero.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## Remarks


If the value of this property is non-zero, it limits resolution of exported raster images. That is, higher-resolution images are resampled down to the limit and lower-resolution images are exported as is.

If the value of this property is zero, all raster images are exported without resampling.

## Examples



Shows how to set limit for image resolution. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## See Also

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
