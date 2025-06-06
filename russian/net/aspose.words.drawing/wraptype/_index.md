---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words для .NET
description: Узнайте, как перечисление Aspose.Words.Drawing.WrapType улучшает обтекание текстом фигур и изображений для профессионального форматирования документов.
type: docs
weight: 1810
url: /ru/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Указывает, как текст обтекает фигуру или изображение.

```csharp
public enum WrapType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `3` | Текст не обтекает фигуру. Фигура расположена за или перед текстом. |
| Inline | `0` | Фигура остается на том же слое, что и текст, и рассматривается как символ. |
| TopBottom | `1` | Текст останавливается в верхней части фигуры и возобновляется на строке под фигурой. |
| Square | `2` | Обтекает текстом все стороны квадратной ограничивающей рамки фигуры. |
| Tight | `4` | Плотно обтекает края фигуры, а не ограничивающий прямоугольник. |
| Through | `5` | То же, что и Tight, но охватывает все открытые части фигуры. |

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

* property [WrapType](../shapebase/wraptype/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
