---
title: PclSaveOptions.RasterizeTransformedElements
second_title: Справочник по API Aspose.Words для .NET
description: PclSaveOptions свойство. Получает или задает значение определяющее следует ли растрировать сложные преобразованные элементы перед сохранением в документ PCL. Значение по умолчаниюистинный .
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Получает или задает значение, определяющее, следует ли растрировать сложные преобразованные элементы перед сохранением в документ PCL. Значение по умолчанию:`истинный` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

### Примечания

PCL не поддерживает некоторые виды преобразований, которые используются Aspose Words. Например, повернутые, перекошенные изображения и текстурные кисти. Для правильного рендеринга таких элементов используется процесс растеризации, т.е. сохранение в изображение и обрезка. Этот процесс может занять дополнительное время и память. Если установлен флаг`ЛОЖЬ` некоторый контент в выводе может отличаться от исходного документа.

### Примеры

Показывает, как растрировать сложные элементы при сохранении документа в PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Смотрите также

* class [PclSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pclsaveoptions/)
* сборка [Aspose.Words](../../../)


