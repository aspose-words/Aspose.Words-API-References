---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью метода Watermark SetImage. Легко добавляйте потрясающие водяные знаки для профессионального штриха.
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
| image | Image | Изображение, отображаемое как водяной знак. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда изображение`нулевой` . |

## Примеры

Показывает, как создать водяной знак из изображения в локальной файловой системе.

```csharp
Document doc = new Document();

            // Измените внешний вид водяного знака изображения с помощью объекта ImageWatermarkOptions,
            // затем передаем его при создании водяного знака из файла изображения.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // У нас есть разные варианты вставки изображения:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

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
| image | Image | Изображение, отображаемое как водяной знак. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда изображение`нулевой` . |

## Примечания

Если[`ImageWatermarkOptions`](../../imagewatermarkoptions/) является`нулевой`, водяной знак будет установлен с параметрами по умолчанию.

## Примеры

Показывает, как создать водяной знак из изображения в локальной файловой системе.

```csharp
Document doc = new Document();

            // Измените внешний вид водяного знака изображения с помощью объекта ImageWatermarkOptions,
            // затем передаем его при создании водяного знака из файла изображения.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // У нас есть разные варианты вставки изображения:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
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

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

Добавляет водяной знак изображения в документ.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imagePath | String | Путь к файлу изображения, отображаемого в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда путь`нулевой` . |

## Примечания

Если[`ImageWatermarkOptions`](../../imagewatermarkoptions/) является`нулевой`, водяной знак будет установлен с параметрами по умолчанию.

## Примеры

Показывает, как создать водяной знак из изображения в локальной файловой системе.

```csharp
Document doc = new Document();

            // Измените внешний вид водяного знака изображения с помощью объекта ImageWatermarkOptions,
            // затем передаем его при создании водяного знака из файла изображения.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // У нас есть разные варианты вставки изображения:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
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

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Добавляет водяной знак изображения в документ.

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageStream | Stream | Поток, содержащий данные изображения, отображаемые в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры для водяного знака изображения. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда путь`нулевой` . |

## Примечания

Если[`ImageWatermarkOptions`](../../imagewatermarkoptions/) является`нулевой`, водяной знак будет установлен с параметрами по умолчанию.

## Примеры

Показывает, как создать водяной знак из потока изображений.

```csharp
Document doc = new Document();

// Измените внешний вид водяного знака изображения с помощью объекта ImageWatermarkOptions,
// затем передаем его при создании водяного знака из файла изображения.
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### Смотрите также

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
