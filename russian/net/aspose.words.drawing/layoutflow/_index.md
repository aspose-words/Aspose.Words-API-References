---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.LayoutFlow для управления макетом текста в текстовых полях, что позволит без труда улучшить дизайн и читабельность документа.
type: docs
weight: 1430
url: /ru/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Определяет поток текста в текстовом поле.

```csharp
public enum LayoutFlow
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Horizontal | `0` | Текст отображается горизонтально. |
| TopToBottomIdeographic | `1` | Идеографический текст отображается вертикально. |
| BottomToTop | `2` | Текст отображается вертикально. |
| TopToBottom | `3` | Текст отображается вертикально. |
| HorizontalIdeographic | `4` | Идеографический текст отображается горизонтально. |
| Vertical | `5` | Текст отображается вертикально. |

## Примеры

Показывает, как добавить текст в текстовое поле и изменить его ориентацию.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100,
    Height = 100
};
textbox.TextBox.LayoutFlow = LayoutFlow.BottomToTop;

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### Смотрите также

* property [LayoutFlow](../textbox/layoutflow/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
