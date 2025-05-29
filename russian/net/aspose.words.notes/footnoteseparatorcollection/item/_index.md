---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Воспользуйтесь свойством FootnoteSeparatorCollection Item, чтобы легко извлекать настроенные разделители сносок по типу, улучшая форматирование документа.
type: docs
weight: 20
url: /ru/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

Извлекает[`FootnoteSeparator`](../../footnoteseparator/) указанного типа.

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## Примечания

Возврат`нулевой` если разделитель сносок/концевых сносок указанного типа не найден.

## Примеры

Показывает, как управлять форматом разделителя сносок.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Выровнять разделитель сносок.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Смотрите также

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
