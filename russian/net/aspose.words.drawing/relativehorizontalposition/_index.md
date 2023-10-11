---
title: Enum RelativeHorizontalPosition
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.RelativeHorizontalPosition перечисление. Указывает относительное горизонтальное положение фигуры или текстового фрейма.
type: docs
weight: 1190
url: /ru/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Указывает относительное горизонтальное положение фигуры или текстового фрейма.

```csharp
public enum RelativeHorizontalPosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Margin | `0` | Указывает, что горизонтальное расположение должно быть относительно полей страницы. |
| Page | `1` | Объект расположен относительно левого края страницы. |
| Column | `2` | Объект расположен относительно левой части столбца. |
| Character | `3` | Объект располагается относительно левой части абзаца. |
| LeftMargin | `4` | Указывает, что горизонтальное расположение должно быть относительно левого поля страницы. |
| RightMargin | `5` | Указывает, что горизонтальное расположение должно быть относительно правого поля страницы. |
| InsideMargin | `6` | Указывает, что горизонтальное расположение должно быть относительно внутреннего поля текущей страницы (левое поле на нечетных страницах, правое на четных страницах). |
| OutsideMargin | `7` | Указывает, что горизонтальное расположение должно быть относительно внешнего поля текущей страницы (правое поле на нечетных страницах, левое на четных страницах). |
| Default | `2` | Значение по умолчанию:Column . |

### Примеры

Показывает, как вставить плавающее изображение в центр страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем плавающее изображение, которое появится за перекрывающимся текстом, и выравниваем его по центру страницы.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Показывает, как вставить изображение и использовать его в качестве водяного знака.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем изображение в заголовок, чтобы оно было видно на каждой странице.
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Размещаем изображение в центре страницы.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Показывает, как вставить изображение и использовать его в качестве водяного знака (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем изображение в заголовок, чтобы оно было видно на каждой странице.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Размещаем изображение в центре страницы.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### Смотрите также

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


