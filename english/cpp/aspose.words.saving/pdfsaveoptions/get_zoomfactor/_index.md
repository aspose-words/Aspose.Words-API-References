---
title: get_ZoomFactor
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining zoom factor (in percentages) for a document.
type: docs
weight: 404
url: /cpp/aspose.words.saving/pdfsaveoptions/get_zoomfactor/
---
## PdfSaveOptions::get_ZoomFactor method


Gets or sets a value determining zoom factor (in percentages) for a document.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_ZoomFactor() const
```


## Examples



Shows how to set the default zooming that a reader applies when opening a rendered PDF document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "ZoomBehavior" property to "PdfZoomBehavior.ZoomFactor" to get a PDF reader to
// apply a percentage-based zoom factor when we open the document with it.
// Set the "ZoomFactor" property to "25" to give the zoom factor a value of 25%.
auto options = MakeObject<PdfSaveOptions>();
options->set_ZoomBehavior(PdfZoomBehavior::ZoomFactor);
options->set_ZoomFactor(25);

// When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
doc->Save(ArtifactsDir + u"PdfSaveOptions.ZoomBehaviour.pdf", options);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
