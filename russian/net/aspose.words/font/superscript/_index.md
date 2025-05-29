---
title: Font.Superscript
linktitle: Superscript
articleTitle: Superscript
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Superscript, легко форматируйте текст как верхний индекс для улучшения читаемости и стиля в ваших документах. Улучшите свой дизайн сегодня!
type: docs
weight: 450
url: /ru/net/aspose.words/font/superscript/
---
## Font.Superscript property

True, если шрифт отформатирован как верхний индекс.

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
