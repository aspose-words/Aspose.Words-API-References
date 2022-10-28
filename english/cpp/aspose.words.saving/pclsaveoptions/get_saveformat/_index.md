---
title: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies the format in which the document will be saved if this save options object is used. Can only be Pcl.
type: docs
weight: 53
url: /cpp/aspose.words.saving/pclsaveoptions/get_saveformat/
---
## PclSaveOptions.get_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be **Pcl**.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PclSaveOptions::get_SaveFormat() override
```


## Examples




Shows how to rasterize complex elements while saving a document to PCL. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

auto saveOptions = MakeObject<PclSaveOptions>();
saveOptions->set_SaveFormat(SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(ArtifactsDir + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

