---
title: PdfSaveOptions.PreblendImages
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Получает или задает значение определяющее следует ли предварительно смешивать прозрачные изображения с черным цветом фона.
type: docs
weight: 260
url: /ru/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

Получает или задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным цветом фона.

```csharp
public bool PreblendImages { get; set; }
```

### Примечания

Предварительное смешивание изображений может улучшить внешний вид PDF-документа в Adobe Reader и удалить артефакты сглаживания.

Чтобы правильно отображать предварительно смешанные изображения, приложение просмотра PDF должно поддерживать запись /Matte в словаре изображений с мягкой маской. Кроме того, предварительное смешивание изображений может снизить производительность рендеринга PDF.

Значение по умолчанию:`ЛОЖЬ`.

### Примеры

Показывает, как предварительно смешать изображения с прозрачным фоном при сохранении документа в формате PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства PreblendImages значение true, чтобы предварительно смешать прозрачные изображения.
// с фоном, который может уменьшить количество артефактов.
// Установите для свойства «PreblendImages» значение «false», чтобы нормально отображать прозрачные изображения.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

Показывает, как предварительно смешивать изображения с прозрачным фоном (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства PreblendImages значение true, чтобы предварительно смешать прозрачные изображения.
// с фоном, который может уменьшить количество артефактов.
// Установите для свойства «PreblendImages» значение «false», чтобы нормально отображать прозрачные изображения.
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


