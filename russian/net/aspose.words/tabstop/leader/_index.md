---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words для .NET
description: Откройте для себя свойства TabStop Leader, чтобы настроить типы линий выноски для ваших вкладок, улучшая ясность и презентацию документа. Оптимизируйте форматирование сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Возвращает или задает тип линии выноски, отображаемой под символом табуляции.

```csharp
public TabLeader Leader { get; set; }
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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
