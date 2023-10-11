---
title: StructuredDocumentTag.WordOpenXMLMinimal
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag свойство. Получает строку представляющую XML содержащийся в узле вFlatOpc format. В отличие отWordOpenXMLСвойство этот метод создает урезанный документ который исключает любые части не связанные с содержанием.
type: docs
weight: 310
url: /ru/net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

Получает строку, представляющую XML, содержащийся в узле вFlatOpc format. В отличие от[`WordOpenXML`](../wordopenxml/)Свойство этот метод создает урезанный документ, который исключает любые части, не связанные с содержанием.

```csharp
public string WordOpenXMLMinimal { get; }
```

### Примеры

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

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


