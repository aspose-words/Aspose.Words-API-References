---
title: Merger.MergeToImages
linktitle: MergeToImages
articleTitle: MergeToImages
second_title: Aspose.Words для .NET
description: С легкостью объединяйте несколько документов с помощью метода MergeToImages, создавая единое выходное изображение, настраивая имена файлов и параметры сохранения.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/merger/mergetoimages/
---
## MergeToImages(*string[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages_1}

Объединяет указанные входные документы в один выходной документ, используя указанные имена входных и выходных файлов и параметры сохранения. Преобразует выходные данные в изображения.

```csharp
public static Stream[] MergeToImages(string[] inputFiles, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFiles | String[] | Имена входных файлов. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| mergeFormatMode | MergeFormatMode | Указывает, как объединить конфликтующее форматирование. |

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## MergeToImages(*Stream[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages}

Объединяет указанные потоки входных документов в один выходной документ, используя указанные параметры сохранения изображений. Преобразует выходные данные в изображения.

```csharp
public static Stream[] MergeToImages(Stream[] inputStreams, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStreams | Stream[] | Входной файл потокового воспроизведения. |
| saveOptions | ImageSaveOptions | Параметры сохранения. |
| mergeFormatMode | MergeFormatMode | Указывает, как объединить конфликтующее форматирование. |

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
