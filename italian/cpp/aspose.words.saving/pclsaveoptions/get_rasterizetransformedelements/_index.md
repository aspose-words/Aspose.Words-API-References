---
title: "Metodo Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements"
linktitle: "get_RasterizeTransformedElements"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements. Ottiene o imposta un valore che determina se gli elementi trasformati complessi debbano essere rasterizzati prima di salvare il documento PCL. Il valore predefinito è true in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Ottiene o imposta un valore che determina se gli elementi trasformati complessi debbano o meno essere rasterizzati prima di salvare il documento PCL. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```


## Esempi



Mostra come rasterizzare elementi complessi durante il salvataggio di un documento in PCL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## Vedi anche

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
