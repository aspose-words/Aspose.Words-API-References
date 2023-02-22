---
title: Enum RelativeVerticalPosition
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.RelativeVerticalPosition перечисление. Указывает относительное положение фигуры или текстового фрейма по вертикали.
type: docs
weight: 1070
url: /ru/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Указывает относительное положение фигуры или текстового фрейма по вертикали.

```csharp
public enum RelativeVerticalPosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Margin | `0` | Указывает, что вертикальное позиционирование должно быть относительно полей страницы. |
| Page | `1` | Объект расположен относительно верхнего края страницы. |
| Paragraph | `2` | Объект позиционируется относительно верхней части абзаца, содержащего привязку. |
| Line | `3` | Недокументировано. |
| TopMargin | `4` | Указывает, что вертикальное позиционирование должно быть относительно верхнего поля текущей страницы. |
| BottomMargin | `5` | Указывает, что вертикальное позиционирование должно быть относительно нижнего поля текущей страницы. |
| InsideMargin | `6` | Указывает, что вертикальное позиционирование должно быть относительно внутреннего поля текущей страницы. |
| OutsideMargin | `7` | Указывает, что вертикальное позиционирование должно быть относительно внешнего поля текущей страницы. |
| TableDefault | `0` | Значение по умолчанию:Margin . |
| TextFrameDefault | `2` | Значение по умолчанию:Paragraph . |

### Примеры

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

Показывает, как вставить изображение и использовать его в качестве водяного знака.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем изображение в шапку, чтобы оно было видно на каждой странице.
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Поместите изображение в центр страницы.
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

// Вставляем изображение в шапку, чтобы оно было видно на каждой странице.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Поместите изображение в центр страницы.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### Смотрите также

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


