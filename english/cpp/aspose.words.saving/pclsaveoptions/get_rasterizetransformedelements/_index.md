---
title: Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements method
linktitle: get_RasterizeTransformedElements
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements method. Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is true in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```


## Examples



Shows how to rasterize complex elements while saving a document to PCL. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## See Also

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
