---
title: "метод Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements"
linktitle: "get_RasterizeTransformedElements"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements. Получает или задает значение, определяющее, следует ли растеризовать сложные трансформированные элементы перед сохранением в документ PCL. По умолчанию true в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Получает или задает значение, определяющее, следует ли растеризовать сложные трансформированные элементы перед сохранением в документ PCL. По умолчанию **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```


## Примеры



Показывает, как растеризовать сложные элементы при сохранении документа в PCL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## См. также

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
