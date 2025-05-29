---
title: TabStopCollection.RemoveByPosition
linktitle: RemoveByPosition
articleTitle: RemoveByPosition
second_title: Aspose.Words для .NET
description: Легко удаляйте позиции табуляции из вашей коллекции с помощью метода RemoveByPosition. Оптимизируйте форматирование для улучшенного контроля над документами!
type: docs
weight: 120
url: /ru/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

Удаляет табуляцию в указанной позиции из коллекции.

```csharp
public void RemoveByPosition(double position)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | Double | Положение (в пунктах) позиции табуляции, которую необходимо удалить. |

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

* class [TabStopCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
