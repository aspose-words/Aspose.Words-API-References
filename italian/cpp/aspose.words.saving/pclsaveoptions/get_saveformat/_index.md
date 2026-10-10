---
title: "Metodo Aspose::Words::Saving::PclSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PclSaveOptions::get_SaveFormat. Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere solo Pcl in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/pclsaveoptions/get_saveformat/
---
## PclSaveOptions::get_SaveFormat method


Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere solo [Pcl](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PclSaveOptions::get_SaveFormat() override
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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
