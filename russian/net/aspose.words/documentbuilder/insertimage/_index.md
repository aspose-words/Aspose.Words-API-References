---
title: InsertImage
second_title: Справочник по API Aspose.Words для .NET
description: Вставляет изображение из .NETImage объект в документ. Изображение вставляется в строку и в масштабе 100.
type: docs
weight: 350
url: /ru/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(Image) {#insertimage_3}

Вставляет изображение из .NETImage объект в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(Image image)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из объекта в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Ниже приведены три способа вставки изображения из экземпляра объекта Image.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(string) {#insertimage_9}

Вставляет изображение из файла или URL-адреса в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Файл с изображением. Может быть любым допустимым локальным или удаленным URI. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Эта перегрузка автоматически загружает изображение перед вставкой в документ если вы укажете удаленный URI.

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить gif-изображение в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

Показывает, как вставить фигуру с изображением в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

Показывает, как вставить плавающее изображение в центр страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

Показывает, как определить, какое изображение будет вставлено.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

Показывает, как вставить изображение из локальной файловой системы в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(Stream) {#insertimage_6}

Вставляет изображение из потока в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий изображение. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить фигуру с изображением из потока в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из потока.
    // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Встроенная форма с пользовательскими размерами:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Плавающая форма с пользовательскими размерами:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

Показывает, как вставить изображение из потока в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из потока.
    // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Встроенная форма с пользовательскими размерами:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Плавающая форма с пользовательскими размерами:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(byte[]) {#insertimage}

Вставляет изображение из байтового массива в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | Byte[] | Массив байтов, содержащий изображение. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из байтового массива в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Ниже приведены три способа вставки изображения из массива байтов.
            // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Встроенная форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Плавающая форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

Показывает, как вставить изображение из байтового массива в документ (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Ниже приведены три способа вставки изображения из массива байтов.
            // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Встроенная форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Плавающая форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(Image, double, double) {#insertimage_5}

Вставляет встроенное изображение из объекта .NETImage в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из объекта в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из экземпляра объекта Image.
    // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Встроенная форма с пользовательскими размерами:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Плавающая форма с пользовательскими размерами:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

Показывает, как вставить изображение из объекта в документ (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из экземпляра объекта Image.
    // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Встроенная форма с пользовательскими размерами:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Плавающая форма с пользовательскими размерами:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(string, double, double) {#insertimage_11}

Вставляет встроенное изображение из файла или URL-адреса в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Файл, содержащий изображение. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из локальной файловой системы в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(Stream, double, double) {#insertimage_8}

Вставляет встроенное изображение из потока в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий изображение. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из потока в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из потока.
    // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Встроенная форма с пользовательскими размерами:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Плавающая форма с пользовательскими размерами:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(byte[], double, double) {#insertimage_2}

Вставляет встроенное изображение из байтового массива в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | Byte[] | Массив байтов, содержащий изображение. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из байтового массива в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Ниже приведены три способа вставки изображения из массива байтов.
            // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Встроенная форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Плавающая форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

Показывает, как вставить изображение из байтового массива в документ (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Ниже приведены три способа вставки изображения из массива байтов.
            // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Встроенная форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Плавающая форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_4}

Вставляет изображение из объекта .NETImage в указанную позицию и размер.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в пунктах от начала координат до левой стороны изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из объекта в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из экземпляра объекта Image.
    // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Встроенная форма с пользовательскими размерами:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Плавающая форма с пользовательскими размерами:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

Показывает, как вставить изображение из объекта в документ (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из экземпляра объекта Image.
    // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Встроенная форма с пользовательскими размерами:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Плавающая форма с пользовательскими размерами:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_10}

Вставляет изображение из файла или URL-адреса в указанной позиции и размере.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Файл, содержащий изображение. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в пунктах от начала координат до левой стороны изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

Показывает, как вставить изображение из локальной файловой системы в документ с сохранением его размеров.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

Показывает, как вставить изображение из локальной файловой системы в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из имени файла локальной системы.
// 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_7}

Вставляет изображение из потока в указанной позиции и размере.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий изображение. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в пунктах от начала координат до левой стороны изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из потока в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из потока.
    // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Встроенная форма с пользовательскими размерами:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Плавающая форма с пользовательскими размерами:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

---

## InsertImage(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_1}

Вставляет изображение из байтового массива в указанной позиции и размера.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | Byte[] | Массив байтов, содержащий изображение. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в пунктах от начала координат до левой стороны изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape)объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из байтового массива в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Ниже приведены три способа вставки изображения из массива байтов.
            // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Встроенная форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Плавающая форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

Показывает, как вставить изображение из байтового массива в документ (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Декодирование изображения преобразует его в формат .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Ниже приведены три способа вставки изображения из массива байтов.
            // 1 — встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Встроенная форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Плавающая форма с пользовательскими размерами:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* пространство имен [Aspose.Words](../../documentbuilder)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
