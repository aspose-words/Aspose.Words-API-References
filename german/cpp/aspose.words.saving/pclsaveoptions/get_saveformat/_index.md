---
title: "Aspose::Words::Saving::PclSaveOptions::get_SaveFormat Methode"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PclSaveOptions::get_SaveFormat Methode. Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionen‑Objekt verwendet wird. Kann nur Pcl in C++ sein."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/pclsaveoptions/get_saveformat/
---
## PclSaveOptions::get_SaveFormat method


Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionen‑Objekt verwendet wird. Kann nur [Pcl](../../../aspose.words/saveformat/) sein.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PclSaveOptions::get_SaveFormat() override
```


## Beispiele



Zeigt, wie komplexe Elemente beim Speichern eines Dokuments in PCL gerastert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
