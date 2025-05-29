---
title: ParagraphFormat.TabStops
linktitle: TabStops
articleTitle: TabStops
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat TabStops, которое позволяет легко управлять пользовательскими позициями табуляции, улучшая форматирование документа и повышая его читабельность.
type: docs
weight: 400
url: /ru/net/aspose.words/paragraphformat/tabstops/
---
## ParagraphFormat.TabStops property

Получает коллекцию пользовательских позиций табуляции, определенных для этого объекта.

```csharp
public TabStopCollection TabStops { get; }
```

## Примеры

Показывает, как изменить положение правой позиции табуляции в абзацах, связанных с оглавлением.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Пройти по всем абзацам со стилями, основанными на результате TOC; это любой стиль между TOC и TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Получаем первую табуляцию, используемую в этом абзаце. Это должна быть табуляция, используемая для выравнивания номеров страниц.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Заменить первую остановку табуляции по умолчанию на пользовательскую остановку табуляции.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Смотрите также

* class [TabStopCollection](../../tabstopcollection/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
