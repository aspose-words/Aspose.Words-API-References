---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words для .NET
description: PclSaveOptions RasterizeTransformedElements свойство. Получает или задает значение определяющее следует ли растрировать сложные преобразованные элементы перед сохранением в документе PCL. Значение по умолчаниюистинный  на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Получает или задает значение, определяющее, следует ли растрировать сложные преобразованные элементы перед сохранением в документе PCL. Значение по умолчанию:`истинный` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Примечания

PCL не поддерживает некоторые виды преобразований, которые используются в Aspose Words. Например, повернутые, перекошенные изображения и текстурные кисти. Для правильной визуализации таких элементов используется процесс растеризации, т.е. сохранение в изображение и обрезка. Этот процесс может занять дополнительное время и память. Если флаг установлен в значение`ЛОЖЬ` , некоторое содержимое вывода может отличаться от исходного документа.

## Примеры

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
