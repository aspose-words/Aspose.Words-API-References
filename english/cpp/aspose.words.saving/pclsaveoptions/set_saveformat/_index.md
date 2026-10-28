---
title: Aspose::Words::Saving::PclSaveOptions::set_SaveFormat method
linktitle: set_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PclSaveOptions::set_SaveFormat method. Specifies the format in which the document will be saved if this save options object is used. Can only be Pcl in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.saving/pclsaveoptions/set_saveformat/
---
## PclSaveOptions::set_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be [Pcl](../../../aspose.words/saveformat/).

```cpp
void Aspose::Words::Saving::PclSaveOptions::set_SaveFormat(Aspose::Words::SaveFormat value) override
```

## Examples


Shows how to rasterize complex elements while saving a document to PCL.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```
## See Also

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
