---
title: get_ZoomBehavior
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer.
type: docs
weight: 391
url: /cpp/aspose.words.saving/pdfsaveoptions/get_zoombehavior/
---
## PdfSaveOptions.get_ZoomBehavior method


Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer.

```cpp
Aspose::Words::Saving::PdfZoomBehavior Aspose::Words::Saving::PdfSaveOptions::get_ZoomBehavior() const
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

