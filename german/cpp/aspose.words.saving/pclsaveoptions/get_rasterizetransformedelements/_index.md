---
title: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements Methode"
linktitle: "get_RasterizeTransformedElements"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob komplexe transformierte Elemente vor dem Speichern in ein PCL‑Dokument gerastert werden sollen oder nicht. Standard ist true in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Liest oder setzt einen Wert, der bestimmt, ob komplexe transformierte Elemente vor dem Speichern in ein PCL-Dokument gerastert werden sollen oder nicht. Standardwert ist **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
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

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
