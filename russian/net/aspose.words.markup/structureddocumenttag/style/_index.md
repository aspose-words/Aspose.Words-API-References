---
title: StructuredDocumentTag.Style
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag свойство. Получает или задает стиль тега структурированного документа.
type: docs
weight: 260
url: /ru/net/aspose.words.markup/structureddocumenttag/style/
---
## StructuredDocumentTag.Style property

Получает или задает стиль тега структурированного документа.

```csharp
public Style Style { get; set; }
```

### Примечания

Только Character стиль илиParagraph можно установить стиль со связанным стилем символов.

### Примеры

Показывает, как работать со стилями для элементов управления содержимым.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа применения стиля из документа к тегу структурированного документа.
// 1 - Применить объект стиля из коллекции стилей документа:
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

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Смотрите также

* class [Style](../../../aspose.words/style/)
* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


