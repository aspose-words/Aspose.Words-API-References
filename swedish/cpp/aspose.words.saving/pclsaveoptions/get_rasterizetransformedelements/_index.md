---
title: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements metod"
linktitle: "get_RasterizeTransformedElements"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements metod. Hämtar eller anger ett värde som bestämmer om komplexa transformerade element ska rasteriseras innan de sparas till ett PCL‑dokument. Standard är true i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Hämtar eller anger ett värde som bestämmer om komplexa transformerade element ska rasteriseras innan de sparas till ett PCL-dokument. Standard är **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```


## Exempel



Visar hur man rasteriserar komplexa element när ett dokument sparas till PCL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## Se även

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
