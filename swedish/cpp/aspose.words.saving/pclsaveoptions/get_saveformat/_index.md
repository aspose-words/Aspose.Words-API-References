---
title: "Aspose::Words::Saving::PclSaveOptions::get_SaveFormat metod"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PclSaveOptions::get_SaveFormat metod. Anger det format som dokumentet kommer att sparas i om detta spara‑alternativ‑objekt används. Kan endast vara Pcl i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/pclsaveoptions/get_saveformat/
---
## PclSaveOptions::get_SaveFormat method


Anger det format som dokumentet kommer att sparas i om detta spara‑alternativ‑objekt används. Kan endast vara [Pcl](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PclSaveOptions::get_SaveFormat() override
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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
