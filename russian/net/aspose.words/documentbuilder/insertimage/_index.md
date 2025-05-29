---
title: DocumentBuilder.InsertImage
linktitle: InsertImage
articleTitle: InsertImage
second_title: Aspose.Words для .NET
description: С легкостью улучшайте свои документы с помощью метода InsertImage в DocumentBuilder, позволяющего легко вставлять изображения .NET в полном масштабе для создания потрясающих визуальных эффектов.
type: docs
weight: 400
url: /ru/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(*Image*) {#insertimage_3}

Вставляет изображение из .NETImage Объект в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(Image image)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из объекта в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Ниже приведены три способа вставки изображения из экземпляра объекта Image.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*string*) {#insertimage_9}

Вставляет изображение из файла или URL в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Файл с изображением. Может быть любым допустимым локальным или удаленным URI. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Эта перегрузка автоматически загрузит изображение перед вставкой в document , если вы укажете удаленный URI.

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение WebP.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "WebP image.webp");

doc.Save(ArtifactsDir + "Image.InsertWebpImage.docx");
```

Показывает, как вставить GIF-изображение в документ.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Мы можем вставить gif-изображение, используя путь или массив байтов.
// Работает только если DocumentBuilder оптимизирован для Word версии 2010 или выше.
// Обратите внимание, что доступ к байтам изображения приводит к преобразованию Gif в PNG.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Показывает, как вставить в документ фигуру с изображением.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два места, где метод "InsertShape" конструктора документов
// можно получить изображение, которое будет отображаться в форме.
// 1 — Передать имя файла изображения в локальной файловой системе:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 — Передать URL-адрес, указывающий на изображение.
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

// Aspose.Words вставляет изображение SVG в документ как PNG с расширением svgBlip
// содержащий исходное векторное представление изображения SVG.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words вставляет изображение SVG в документ как PNG, так же, как это делает Microsoft Word для старого формата.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words вставляет изображение SVG в документ как метафайл EMF, чтобы сохранить изображение в векторном представлении.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Показывает, как вставить изображение из локальной файловой системы в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из локального системного имени файла.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*Stream*) {#insertimage_6}

Вставляет изображение из потока в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий изображение. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

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
    // 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 — Встроенная форма с пользовательскими размерами:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 — Плавающая форма с пользовательскими размерами:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*byte[]*) {#insertimage}

Вставляет изображение из массива байтов в документ. Изображение вставляется в строку и в масштабе 100%.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | Byte[] | Массив байтов, содержащий изображение. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из байтового массива в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Ниже приведены три способа вставки изображения из байтового массива.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*Image, double, double*) {#insertimage_5}

Вставляет встроенное изображение из .NETImage объект в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из объекта в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Ниже приведены три способа вставки изображения из экземпляра объекта Image.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*string, double, double*) {#insertimage_11}

Вставляет встроенное изображение из файла или URL в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Файл, содержащий изображение. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из локальной файловой системы в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из локального системного имени файла.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*Stream, double, double*) {#insertimage_8}

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

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из потока в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из потока.
    // 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 — Встроенная форма с пользовательскими размерами:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 — Плавающая форма с пользовательскими размерами:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*byte[], double, double*) {#insertimage_2}

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

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из байтового массива в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Ниже приведены три способа вставки изображения из байтового массива.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*Image, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_4}

Вставляет изображение из .NETImage Объект в указанном положении и размере.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Изображение для вставки в документ. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в точках от начала координат до левой стороны изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в точках от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из объекта в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Ниже приведены три способа вставки изображения из экземпляра объекта Image.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_10}

Вставляет изображение из файла или URL в указанное положение и размер.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Файл, содержащий изображение. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в точках от начала координат до левой стороны изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в точках от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Существует два способа использования конструктора документов для получения изображения и его последующей вставки в виде плавающей фигуры.
// 1 - Из файла в локальной файловой системе:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Из URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Показывает, как вставить изображение из локальной файловой системы в документ, сохранив его размеры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Метод InsertImage создает плавающую фигуру с переданным изображением в данных изображения.
// Мы можем указать размеры фигуры, передав их этому методу.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Передача отрицательных значений в качестве предполагаемых измерений автоматически определит
// размеры фигуры основаны на размерах ее изображения.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Показывает, как вставить изображение из локальной файловой системы в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три способа вставки изображения из локального системного имени файла.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*Stream, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_7}

Вставляет изображение из потока в указанную позицию и размер.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий изображение. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в точках от начала координат до левой стороны изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в точках от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из потока в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Ниже приведены три способа вставки изображения из потока.
    // 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 — Встроенная форма с пользовательскими размерами:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 — Плавающая форма с пользовательскими размерами:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertImage(*byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_1}

Вставляет изображение из массива байтов в указанную позицию и размер.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | Byte[] | Массив байтов, содержащий изображение. |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | Double | Расстояние в точках от начала координат до левой стороны изображения. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | Double | Расстояние в точках от начала координат до верхней стороны изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | WrapType | Указывает, как обтекать изображение текстом. |

### Возвращаемое значение

Узел изображения, который был только что вставлен.

## Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

## Примеры

Показывает, как вставить изображение из байтового массива в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Ниже приведены три способа вставки изображения из байтового массива.
// 1 — Встроенная фигура с размером по умолчанию, основанным на исходных размерах изображения:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 — Встроенная форма с пользовательскими размерами:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 — Плавающая форма с пользовательскими размерами:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
