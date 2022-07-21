---
title: InsertImage
second_title: Справочник по API Aspose.Words для .NET
description: Вставляет изображение из .NETImage в документ. Изображение вставляется в строку и в масштабе 100.
type: docs
weight: 350
url: /ru/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(Image) {#insertimage_3}

Вставляет изображение из .NETImage в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(Image image)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

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

Эта перегрузка автоматически загрузит изображение перед вставкой в document , если вы укажете удаленный URI.

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить gif-изображение в документ.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Мы можем вставить gif-изображение, используя путь или массив байтов.
// Это работает, только если DocumentBuilder оптимизирован для Word версии 2010 или выше.
// Обратите внимание, что доступ к байтам изображения вызывает преобразование Gif в Png.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Показывает, как вставить фигуру с изображением в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два места, где метод "InsertShape" построителя документа
// можно получить изображение, которое будет отображаться в форме.
// 1 - Передать имя файла изображения в локальной файловой системе:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - Передайте URL, который указывает на изображение.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Показывает, как вставить плавающее изображение в центр страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте плавающее изображение, которое будет отображаться за перекрывающимся текстом, и выровняйте его по центру страницы.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Показывает, как определить, какое изображение будет вставлено.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words вставляет SVG-изображение в документ в формате PNG с расширением svgBlip
// который содержит исходное представление векторного изображения SVG.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words вставляет SVG-изображение в документ в формате PNG, точно так же, как это делает Microsoft Word для старого формата.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words вставляет изображение SVG в документ как метафайл EMF, чтобы сохранить изображение в векторном представлении.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
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

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить фигуру с изображением из потока в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
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

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из массива байтов в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

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

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Показывает, как вставить изображение из массива байтов в документ (.NetStandard 2.0).

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

Вставляет встроенное изображение из .NETImage объект в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

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
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

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
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

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

Вставляет встроенное изображение из массива байтов в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | Byte[] | Массив байтов, содержащий изображение. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из массива байтов в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

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

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Показывает, как вставить изображение из массива байтов в документ (.NetStandard 2.0).

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

Вставляет изображение из .NETImage объект в указанной позиции и размере.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в пунктах от начала координат до левого края изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

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
| left | Double | Расстояние в пунктах от начала координат до левого края изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Есть два способа использования конструктора документов для получения изображения и его последующей вставки в виде плавающей формы.
// 1 - Из файла в локальной файловой системе:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Из URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Показывает, как вставить изображение из локальной файловой системы в документ с сохранением его размеров.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Метод InsertImage создает плавающую фигуру с переданным изображением в данных изображения.
// Мы можем указать размеры фигуры, передав их этому методу.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Передача отрицательных значений в качестве предполагаемых размеров автоматически определит
// размеры фигуры на основе размеров ее изображения.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
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
| left | Double | Расстояние в пунктах от начала координат до левого края изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

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

Вставляет изображение из массива байтов в указанной позиции и размере.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | Byte[] | Массив байтов, содержащий изображение. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в пунктах от начала координат до левого края изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить изображение из массива байтов в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

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

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Показывает, как вставить изображение из массива байтов в документ (.NetStandard 2.0).

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
