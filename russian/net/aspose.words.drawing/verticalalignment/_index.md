---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.VerticalAlignment для точного вертикального выравнивания текстовых фреймов и таблиц в ваших документах. Улучшите контроль макета!
type: docs
weight: 1790
url: /ru/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Задает вертикальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы.

```csharp
public enum VerticalAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Объект явно позиционируется, обычно с использованием его**Вершина** свойство. |
| Top | `1` | Указывает, что объект должен находиться в верхней части вертикальной базы выравнивания. |
| Center | `2` | Указывает, что объект должен быть центрирован относительно вертикальной базы выравнивания. |
| Bottom | `3` | Указывает, что объект должен находиться в нижней части вертикальной базы выравнивания. |
| Inside | `4` | Указывает, что объект должен находиться внутри горизонтальной базы выравнивания. |
| Outside | `5` | Указывает, что объект должен находиться за пределами вертикальной базы выравнивания. |
| Inline | `-1` | Не документировано. Кажется, это возможное значение для плавающих абзацев и таблиц. |
| Default | `0` | То же, что иNone . |

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

### Смотрите также

* property [VerticalAlignment](../shapebase/verticalalignment/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
