---
title: Aspose::Words::Saving::DownsampleOptions class
linktitle: DownsampleOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::DownsampleOptions class. Allows to specify downsample options. To learn more, visit the  documentation article in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class


Allows to specify downsample options. To learn more, visit the [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) documentation article.

```cpp
class DownsampleOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [DownsampleOptions](./downsampleoptions/)() |  |
| [get_DownsampleImages](./get_downsampleimages/)() const | Specifies whether images should be downsampled. |
| [get_Resolution](./get_resolution/)() const | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [get_ResolutionThreshold](./get_resolutionthreshold/)() const | Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DownsampleImages](./set_downsampleimages/)(bool) | Specifies whether images should be downsampled. |
| [set_Resolution](./set_resolution/)(int32_t) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [set_ResolutionThreshold](./set_resolutionthreshold/)(int32_t) | Setter for [Aspose::Words::Saving::DownsampleOptions::get_ResolutionThreshold](./get_resolutionthreshold/). |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
