---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words для .NET
description: Watermark SetImage метод. Добавляет водяной знак изображения в документ на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

Добавляет водяной знак изображения в документ.

```csharp
public void SetImage(Image image)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение, отображаемое в виде водяного знака. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда изображение`нулевой` . |

### Смотрите также

* class [Watermark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

Добавляет водяной знак изображения в документ.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение, отображаемое в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда изображение`нулевой` . |

## Примечания

Если[`ImageWatermarkOptions`](../../imagewatermarkoptions/) является`нулевой`, для водяного знака будут установлены параметры по умолчанию.

## Примеры

Показывает, как создать водяной знак из изображения в локальной файловой системе.

```csharp
Document doc = new Document();

            // Измените внешний вид водяного знака изображения с помощью объекта ImageWatermarkOptions,
            // затем передаем его при создании водяного знака из файла изображения.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Смотрите также

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Добавляет водяной знак изображения в документ.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imagePath | String | Путь к файлу изображения, который отображается в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда путь`нулевой` . |

## Примечания

Если[`ImageWatermarkOptions`](../../imagewatermarkoptions/) является`нулевой`, для водяного знака будут установлены параметры по умолчанию.

### Смотрите также

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
