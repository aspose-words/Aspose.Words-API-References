---
title: Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements method
linktitle: get_RasterizeTransformedElements
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements method. Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is true in C++.'
type: docs
weight: 8668
url: /cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is **true**.

```cpp
_Bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```

## Remarks

 PCL doesn't support some kind of transformations that are used by Aspose Words. E.g. rotated, skewed images and texture brushes. To properly render such elements rasterization process is used, i.e. saving to image and clipping. This process can take additional time and memory. If flag is set to **false**, some content in output may be different as compared with the source document. 
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
