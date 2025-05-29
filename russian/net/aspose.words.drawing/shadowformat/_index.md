---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Drawing.ShadowFormat для улучшенных эффектов тени объекта. Поднимите дизайн документа на новый уровень с помощью настраиваемых параметров форматирования тени.
type: docs
weight: 1620
url: /ru/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

Представляет форматирование тени для объекта.

Чтобы узнать больше, посетите[Работа с графическими элементами](https://docs.aspose.com/words/net/working-with-graphic-elements/) документальная статья.

```csharp
public class ShadowFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | ПолучаетColor объект, представляющий цвет тени. Значение по умолчанию:Black . |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | Получает или задает указанный[`ShadowType`](../shadowtype/) для ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | Возврат`истинный` если форматирование, примененное к этому экземпляру, видимо. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | Очищает теневой формат. |

## Примеры

Показывает, как получить цвет тени.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
