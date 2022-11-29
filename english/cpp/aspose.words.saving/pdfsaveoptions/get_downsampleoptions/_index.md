---
title: get_DownsampleOptions
second_title: Aspose.Words for C++ API Reference
description: Allows to specify downsample options.
type: docs
weight: 131
url: /cpp/aspose.words.saving/pdfsaveoptions/get_downsampleoptions/
---
## PdfSaveOptions::get_DownsampleOptions method


Allows to specify downsample options.

```cpp
System::SharedPtr<Aspose::Words::Saving::DownsampleOptions> Aspose::Words::Saving::PdfSaveOptions::get_DownsampleOptions() const
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

* Class [DownsampleOptions](../../downsampleoptions/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
