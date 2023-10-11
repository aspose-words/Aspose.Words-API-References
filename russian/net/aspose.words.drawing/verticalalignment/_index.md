---
title: Enum VerticalAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.VerticalAlignment перечисление. Определяет вертикальное выравнивание плавающей фигуры текстового фрейма или плавающей таблицы.
type: docs
weight: 1380
url: /ru/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Определяет вертикальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы.

```csharp
public enum VerticalAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Объект позиционируется явно, обычно с использованием его **Вершина** свойство. |
| Top | `1` | Указывает, что объект должен находиться вверху базы вертикального выравнивания. |
| Center | `2` | Указывает, что объект должен быть центрирован относительно базы вертикального выравнивания. |
| Bottom | `3` | Указывает, что объект должен находиться внизу базы вертикального выравнивания. |
| Inside | `4` | Указывает, что объект должен находиться внутри базы горизонтального выравнивания. |
| Outside | `5` | Указывает, что объект должен находиться за пределами базы вертикального выравнивания. |
| Inline | `-1` | Не документировано. Кажется, это возможное значение для плавающих абзацев и таблиц. |
| Default | `0` | То же, что иNone . |

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

* property [VerticalAlignment](../shapebase/verticalalignment/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)


