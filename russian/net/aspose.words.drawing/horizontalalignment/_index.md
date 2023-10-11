---
title: Enum HorizontalAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.HorizontalAlignment перечисление. Указывает горизонтальное выравнивание плавающей фигуры текстового фрейма или плавающей таблицы.
type: docs
weight: 1030
url: /ru/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

Указывает горизонтальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы.

```csharp
public enum HorizontalAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Объект позиционируется явно, обычно с использованием его **Левый** свойство. |
| Default | `0` | То же, что иNone . |
| Left | `1` | Указывает, что объект должен быть выровнен по левому краю по базе горизонтального выравнивания. |
| Center | `2` | Указывает, что объект должен быть центрирован относительно базы горизонтального выравнивания. |
| Right | `3` | Указывает, что объект должен быть выровнен по правому краю относительно базы горизонтального выравнивания. |
| Inside | `4` | Указывает, что объект должен находиться внутри базы горизонтального выравнивания. |
| Outside | `5` | Указывает, что объект должен находиться за пределами базы горизонтального выравнивания. |

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

### Смотрите также

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


