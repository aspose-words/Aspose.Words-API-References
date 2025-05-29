---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Markup.MarkupLevel, определяющее место StructuredDocumentTags в дереве документа для улучшенной организации и контроля.
type: docs
weight: 4670
url: /ru/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Указывает уровень в дереве документа, где находится конкретный[`StructuredDocumentTag`](../structureddocumenttag/) может произойти.

```csharp
public enum MarkupLevel
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Unknown | `0` | Указывает неизвестное или недопустимое значение. |
| Inline | `1` | Элемент находится на уровне строки (например, среди фрагментов текста). |
| Block | `2` | Элемент встречается на уровне блока (например, среди таблиц и абзацев). |
| Row | `3` | Элемент встречается среди строк в таблице. |
| Cell | `4` | Элемент встречается среди ячеек в строке. |

## Примеры

Показывает, как работать со стилями для элементов управления содержимым.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа применения стиля из документа к структурированному тегу документа.
// 1 — Применить объект стиля из коллекции стилей документа:
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
