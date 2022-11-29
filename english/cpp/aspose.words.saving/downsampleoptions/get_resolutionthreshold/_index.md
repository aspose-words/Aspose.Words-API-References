---
title: get_ResolutionThreshold
second_title: Aspose.Words for C++ API Reference
description: Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled.
type: docs
weight: 40
url: /cpp/aspose.words.saving/downsampleoptions/get_resolutionthreshold/
---
## DownsampleOptions::get_ResolutionThreshold method


Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled.

```cpp
int32_t Aspose::Words::Saving::DownsampleOptions::get_ResolutionThreshold() const
```


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

* Class [DownsampleOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
