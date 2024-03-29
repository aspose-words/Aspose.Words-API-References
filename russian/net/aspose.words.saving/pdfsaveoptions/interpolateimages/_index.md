---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words для .NET
description: PdfSaveOptions InterpolateImages свойство. Флаг указывающий должна ли интерполяция изображения выполняться соответствующим считывателем. КогдаЛОЖЬ указан флаг не записывается в выходной документ и вместо него используется поведение чтения по умолчанию на С#.
type: docs
weight: 210
url: /ru/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Флаг, указывающий, должна ли интерполяция изображения выполняться соответствующим считывателем. Когда`ЛОЖЬ` указан, флаг не записывается в выходной документ и вместо него используется поведение чтения по умолчанию.

```csharp
public bool InterpolateImages { get; set; }
```

## Примечания

Когда разрешение исходного изображения значительно ниже разрешения устройства вывода, каждый исходный образец охватывает множество пикселей устройства. В результате изображения могут выглядеть неровными или блочными. Эти визуальные артефакты можно уменьшить, применив алгоритм интерполяции изображения во время рендеринга. Вместо окрашивания всех пикселей, покрытых исходным образцом, в один и тот же цвет, интерполяция изображения пытается создать плавное изображение. переход между соседними значениями выборки.

Соответствующий Reader может отказаться от реализации этой функции PDF, или может использовать любую конкретную реализацию интерполяции, которую он пожелает.

Значение по умолчанию:`ЛОЖЬ`.

Флаг интерполяции запрещен стандартом PDF/A.`ЛОЖЬ` значение будет использоваться автоматически при сохранении в PDF/A.

## Примеры

Показывает, как выполнить интерполяцию изображений при сохранении документа в формате PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства «InterpolateImages» значение «true», чтобы программа чтения, открывающая этот документ, могла интерполировать изображения.
// Их разрешение должно быть ниже, чем у устройства, отображающего документ.
// Установите для свойства «InterpolateImages» значение «false», чтобы средство чтения не применяло интерполяцию.
saveOptions.InterpolateImages = interpolateImages;

// Когда мы откроем этот документ с помощью программы чтения, такой как Adobe Acrobat, нам нужно будет увеличить изображение.
// чтобы увидеть эффект интерполяции, если мы сохранили документ с включенной интерполяцией.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

Показывает, как улучшить качество изображения в визуализированных документах (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства «InterpolateImages» значение «true», чтобы программа чтения, открывающая этот документ, могла интерполировать изображения.
// Их разрешение должно быть ниже, чем у устройства, отображающего документ.
// Установите для свойства «InterpolateImages» значение «false», чтобы средство чтения не применяло интерполяцию.
saveOptions.InterpolateImages = interpolateImages;

// Когда мы откроем этот документ с помощью программы чтения, такой как Adobe Acrobat, нам нужно будет увеличить изображение.
// чтобы увидеть эффект интерполяции, если мы сохранили документ с включенной интерполяцией.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
