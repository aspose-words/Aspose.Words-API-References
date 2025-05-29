---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words для .NET
description: Управляйте растеризацией сложных элементов в документах PCL с помощью PclSaveOptions. Легко управляйте качеством изображения и размером файла для достижения оптимальных результатов.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Возвращает или задает значение, определяющее, следует ли растеризовать сложные преобразованные элементы перед сохранением в документе PCL. Значение по умолчанию:`истинный` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Примечания

PCL не поддерживает некоторые виды преобразований, которые используются Aspose Words. Например, повернутые, перекошенные изображения и текстурные кисти. Для правильной визуализации таких элементов используется процесс растеризации, т.е. сохранение в изображение и обрезка. Этот процесс может занять дополнительное время и память. Если флаг установлен в`ЛОЖЬ` , часть содержимого в выходных данных может отличаться по сравнению с исходным документом.

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
