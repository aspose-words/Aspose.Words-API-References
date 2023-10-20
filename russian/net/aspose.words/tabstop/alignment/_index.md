---
title: TabStop.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words для .NET
description: TabStop Alignment свойство. Получает или задает выравнивание текста на этой позиции табуляции на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/tabstop/alignment/
---
## TabStop.Alignment property

Получает или задает выравнивание текста на этой позиции табуляции.

```csharp
public TabAlignment Alignment { get; set; }
```

## Примеры

Показывает, как изменить положение правой позиции табуляции в абзацах, связанных с содержанием.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Перебираем все абзацы со стилями на основе результатов оглавления; это любой стиль между TOC и TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Получаем первую вкладку, используемую в этом абзаце. Это должна быть вкладка, используемая для выравнивания номеров страниц.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Заменяем первую табуляцию по умолчанию, остановку на пользовательскую позицию табуляции.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Смотрите также

* enum [TabAlignment](../../tabalignment/)
* class [TabStop](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
