---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.RelativeHorizontalPosition, чтобы определить точное горизонтальное расположение фигур и текстовых фреймов в ваших документах.
type: docs
weight: 1580
url: /ru/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Указывает, относительно чего определяется горизонтальное положение фигуры или текстовой рамки.

```csharp
public enum RelativeHorizontalPosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Margin | `0` | Указывает, что горизонтальное позиционирование должно быть относительно полей страницы. |
| Page | `1` | Объект позиционируется относительно левого края страницы. |
| Column | `2` | Объект позиционируется относительно левой стороны столбца. |
| Character | `3` | Объект позиционируется относительно левой стороны абзаца. |
| LeftMargin | `4` | Указывает, что горизонтальное позиционирование должно быть относительно левого поля страницы. |
| RightMargin | `5` | Указывает, что горизонтальное позиционирование должно быть относительно правого поля страницы. |
| InsideMargin | `6` | Указывает, что горизонтальное позиционирование должно быть относительно внутреннего поля текущей страницы (левое поле на нечетных страницах, правое на четных страницах). |
| OutsideMargin | `7` | Указывает, что горизонтальное позиционирование должно быть относительно внешнего поля текущей страницы (правое поле на нечетных страницах, левое на четных страницах). |
| Default | `2` | Значение по умолчанию:Column . |

## Примеры

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

// Вставьте изображение в заголовок, чтобы оно было видно на каждой странице.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Разместите изображение в центре страницы.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Смотрите также

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
