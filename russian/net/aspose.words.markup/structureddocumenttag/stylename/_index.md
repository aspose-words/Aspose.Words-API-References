---
title: StructuredDocumentTag.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StyleName StructuredDocumentTag. Легко управляйте и настраивайте стили для своих документов, чтобы улучшить организацию и ясность.
type: docs
weight: 270
url: /ru/net/aspose.words.markup/structureddocumenttag/stylename/
---
## StructuredDocumentTag.StyleName property

Возвращает или задает имя стиля, примененного к структурированному тегу документа.

```csharp
public string StyleName { get; set; }
```

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

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
