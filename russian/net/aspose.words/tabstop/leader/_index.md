---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words для .NET
description: TabStop Leader свойство. Получает или задает тип линии выноски отображаемой под символом табуляции на С#.
type: docs
weight: 40
url: /ru/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Получает или задает тип линии выноски, отображаемой под символом табуляции.

```csharp
public TabLeader Leader { get; set; }
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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
