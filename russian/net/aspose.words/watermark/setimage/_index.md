---
title: Watermark.SetImage
second_title: Справочник по API Aspose.Words для .NET
description: Watermark метод. Добавляет водяной знак изображения в документ.
type: docs
weight: 30
url: /ru/net/aspose.words/watermark/setimage/
---
## SetImage(Image) {#setimage}

Добавляет водяной знак изображения в документ.

```csharp
public void SetImage(Image image)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение, которое отображается как водяной знак. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда изображение пустое. |

### Смотрите также

* class [Watermark](../)
* пространство имен [Aspose.Words](../../watermark/)
* сборка [Aspose.Words](../../../)

---

## SetImage(Image, ImageWatermarkOptions) {#setimage_1}

Добавляет водяной знак изображения в документ.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение, которое отображается как водяной знак. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры водяного знака изображения. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда изображение пустое. |

### Примечания

Если[`ImageWatermarkOptions`](../../imagewatermarkoptions/) имеет значение null, водяной знак будет установлен с параметрами по умолчанию.

### Примеры

Показывает, как создать водяной знак из изображения в локальной файловой системе.

```csharp
Document doc = new Document();

            // Изменяем внешний вид водяного знака изображения с помощью объекта ImageWatermarkOptions,
            // затем передать его при создании водяного знака из файла изображения.
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
* пространство имен [Aspose.Words](../../watermark/)
* сборка [Aspose.Words](../../../)

---

## SetImage(string, ImageWatermarkOptions) {#setimage_2}

Добавляет водяной знак изображения в документ.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imagePath | String | Путь к файлу изображения, которое отображается в виде водяного знака. |
| options | ImageWatermarkOptions | Определяет дополнительные параметры водяного знака изображения. |

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, когда путь нулевой. |

### Примечания

Если[`ImageWatermarkOptions`](../../imagewatermarkoptions/) имеет значение null, водяной знак будет установлен с параметрами по умолчанию.

### Смотрите также

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* пространство имен [Aspose.Words](../../watermark/)
* сборка [Aspose.Words](../../../)


