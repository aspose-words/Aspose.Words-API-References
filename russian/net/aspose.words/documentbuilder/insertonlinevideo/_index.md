---
title: InsertOnlineVideo
second_title: Справочник по API Aspose.Words для .NET
description: Вставляет объект онлайнвидео в документ и масштабирует его до указанного размера.
type: docs
weight: 390
url: /ru/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | String | URL-адрес видео. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

Поддерживается вставка онлайн-видео со следующих ресурсов:

* https://www.youtube.com/
* https://vimeo.com/

Если ваше онлайн-видео отображается неправильно, используйте[`InsertOnlineVideo`](./insertonlinevideo/), который принимает пользовательский встроенный HTML-код.

Код для встраивания видео может варьироваться в зависимости от провайдера, для получения подробной информации обратитесь к соответствующему провайдеру.

### Примеры

Показывает, как вставить онлайн-видео в документ с помощью URL-адреса.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// Мы можем посмотреть видео из Microsoft Word, нажав на фигуру.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | String | URL-адрес видео. |
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

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

Поддерживается вставка онлайн-видео со следующих ресурсов:

* https://www.youtube.com/
* https://vimeo.com/

Если ваше онлайн-видео отображается неправильно, используйте[`InsertOnlineVideo`](./insertonlinevideo/), который принимает пользовательский встроенный HTML-код.

Код для встраивания видео может варьироваться в зависимости от провайдера, для получения подробной информации обратитесь к соответствующему провайдеру.

### Примеры

Показывает, как вставить онлайн-видео в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Вставьте фигуру, которая воспроизводит видео из Интернета при нажатии в Microsoft Word.
// Эта прямоугольная форма будет содержать изображение, основанное на первом кадре связанного видео
// и визуальная подсказка «кнопка воспроизведения». Видео имеет соотношение сторон 16:9.
// Мы установим размер фигуры в этом соотношении, чтобы изображение не выглядело растянутым.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], double, double) {#insertonlinevideo_3}

Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | String | URL-адрес видео. |
| videoEmbedCode | String | Код для встраивания видео. |
| thumbnailImageBytes | Byte[] | Байты миниатюры изображения. |
| width | Double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | Double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### Возвращаемое значение

Только что вставленный узел изображения.

### Примечания

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить онлайн-видео в документ с настраиваемой миниатюрой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Ниже приведены два способа создания фигуры с настраиваемой миниатюрой, которая ссылается на онлайн-видео.
        // который будет воспроизводиться, когда мы нажимаем на фигуру в Microsoft Word.
        // 1 - Вставьте встроенную фигуру в курсор вставки узла построителя:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Вставить плавающую фигуру:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo_2}

Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | String | URL-адрес видео. |
| videoEmbedCode | String | Код для встраивания видео. |
| thumbnailImageBytes | Byte[] | Байты миниатюры изображения. |
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

Вы можете изменить размер изображения, местоположение, метод позиционирования и другие настройки с помощью [`Shape`](../../../aspose.words.drawing/shape/) объект, возвращаемый этим методом.

### Примеры

Показывает, как вставить онлайн-видео в документ с настраиваемой миниатюрой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Ниже приведены два способа создания фигуры с настраиваемой миниатюрой, которая ссылается на онлайн-видео.
        // который будет воспроизводиться, когда мы нажимаем на фигуру в Microsoft Word.
        // 1 - Вставьте встроенную фигуру в курсор вставки узла построителя:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Вставить плавающую фигуру:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
