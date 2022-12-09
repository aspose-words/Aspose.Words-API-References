---
title: DownsampleOptions
second_title: Aspose.Words for C++ API Reference
description: Allows to specify downsample options. To learn more, visit the  documentation article.
type: docs
weight: 66
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
| [set_DownsampleImages](./set_downsampleimages/)(bool) | Setter for [Aspose::Words::Saving::DownsampleOptions::get_DownsampleImages](./get_downsampleimages/). |
| [set_Resolution](./set_resolution/)(int32_t) | Setter for [Aspose::Words::Saving::DownsampleOptions::get_Resolution](./get_resolution/). |
| [set_ResolutionThreshold](./set_resolutionthreshold/)(int32_t) | Setter for [Aspose::Words::Saving::DownsampleOptions::get_ResolutionThreshold](./get_resolutionthreshold/). |
| static [Type](./type/)() |  |

## Examples



Shows how to change the resolution of images in the PDF document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// By default, Aspose.Words downsample all images in a document that we save to PDF to 220 ppi.
ASSERT_TRUE(options->get_DownsampleOptions()->get_DownsampleImages());
ASSERT_EQ(220, options->get_DownsampleOptions()->get_Resolution());
ASSERT_EQ(0, options->get_DownsampleOptions()->get_ResolutionThreshold());

doc->Save(ArtifactsDir + u"PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Set the "Resolution" property to "36" to downsample all images to 36 ppi.
options->get_DownsampleOptions()->set_Resolution(36);

// Set the "ResolutionThreshold" property to only apply the downsampling to
// images with a resolution that is above 128 ppi.
options->get_DownsampleOptions()->set_ResolutionThreshold(128);

// Only the first two images from the document will be downsampled at this stage.
doc->Save(ArtifactsDir + u"PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
