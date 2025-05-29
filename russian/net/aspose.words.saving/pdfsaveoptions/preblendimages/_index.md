---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PreblendImages в PdfSaveOptions. Легко управляйте прозрачным смешиванием изображений для улучшения качества документа и визуальной привлекательности.
type: docs
weight: 270
url: /ru/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Возвращает или задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным фоновым цветом.

```csharp
public bool PreblendImages { get; set; }
```

## Примечания

Предварительное смешивание изображений может улучшить внешний вид PDF-документа в Adobe Reader и удалить артефакты сглаживания.

Для правильного отображения предварительно смешанных изображений приложение для просмотра PDF-файлов должно поддерживать запись /Matte в словаре изображений с мягкой маской. Кроме того, предварительно смешанные изображения могут снизить производительность рендеринга PDF-файлов.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как предварительно смешивать изображения с прозрачным фоном при сохранении документа в формате PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Установите свойство "PreblendImages" в значение "true" для предварительного смешивания прозрачных изображений
// с фоном, что может уменьшить артефакты.
// Установите свойство «PreblendImages» в значение «false» для обычной визуализации прозрачных изображений.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
