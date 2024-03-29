---
title: Font.Superscript
linktitle: Superscript
articleTitle: Superscript
second_title: Aspose.Words для .NET
description: Font Superscript свойство. True если шрифт отформатирован как надстрочный на С#.
type: docs
weight: 440
url: /ru/net/aspose.words/font/superscript/
---
## Font.Superscript property

True, если шрифт отформатирован как надстрочный.

```csharp
public bool Superscript { get; set; }
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

// Добавляем ряд обычного текста.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Добавляем фрагмент текста, который отображается в виде нижнего индекса.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Добавляем фрагмент текста, который отображается как надстрочный индекс.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
