---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Position, легко настройте выравнивание текста в пунктах для точного контроля над типографикой. Поднимите свой дизайн с помощью гибкого позиционирования!
type: docs
weight: 310
url: /ru/net/aspose.words/font/position/
---
## Font.Position property

Возвращает или задает положение текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, а отрицательное число опускает его.

```csharp
public double Position { get; set; }
```

## Примеры

Показывает, как форматировать текст, чтобы сместить его положение.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Поднимите этот фрагмент текста на 5 пунктов выше базовой линии.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Опустите этот фрагмент текста на 10 пунктов ниже базовой линии.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Добавить строку обычного текста.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Добавьте фрагмент текста, который отображается как нижний индекс.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Добавьте фрагмент текста, который отображается как верхний индекс.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
