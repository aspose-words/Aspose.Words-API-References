---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words для .NET
description: Aspose.Words.Markup.MarkupLevel перечисление. Указывает уровень в дереве документа на котором конкретныйStructuredDocumentTag может произойти на С#.
type: docs
weight: 3980
url: /ru/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Указывает уровень в дереве документа, на котором конкретный[`StructuredDocumentTag`](../structureddocumenttag/) может произойти.

```csharp
public enum MarkupLevel
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Unknown | `0` | Указывает неизвестное или недопустимое значение. |
| Inline | `1` | Элемент встречается на строчном уровне (например, среди фрагментов текста). |
| Block | `2` | Элемент встречается на уровне блока (например, среди таблиц и параграфов). |
| Row | `3` | Элемент встречается среди строк таблицы. |
| Cell | `4` | Элемент встречается среди ячеек подряд. |

## Примеры

Показывает, как работать со стилями элементов управления содержимым.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа применения стиля документа к тегу структурированного документа.
// 1 — применить объект стиля из коллекции стилей документа:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Ссылка на стиль в документе по имени:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Смотрите также

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
