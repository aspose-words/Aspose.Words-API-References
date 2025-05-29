---
title: StructuredDocumentTag.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words для .NET
description: Узнайте, как управлять свойством Style объекта StructuredDocumentTags, чтобы без труда улучшить форматирование документа и повысить его читабельность.
type: docs
weight: 260
url: /ru/net/aspose.words.markup/structureddocumenttag/style/
---
## StructuredDocumentTag.Style property

Возвращает или задает стиль тега структурированного документа.

```csharp
public Style Style { get; set; }
```

## Примечания

ТолькоCharacter стиль илиParagraph можно задать стиль со связанным стилем символа.

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

* class [Style](../../../aspose.words/style/)
* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
