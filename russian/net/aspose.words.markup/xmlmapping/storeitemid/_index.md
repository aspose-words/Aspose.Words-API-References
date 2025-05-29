---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: Aspose.Words для .NET
description: Откройте для себя свойство XmlMapping StoreItemId для пользовательских идентификаторов данных XML. Улучшите оценку XPath с помощью наших уникальных решений для эффективного управления данными.
type: docs
weight: 40
url: /ru/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Указывает пользовательский идентификатор данных XML для пользовательской части данных XML, которая будет использоваться для оценки[`XPath`](../xpath/) выражение.

```csharp
public string StoreItemId { get; }
```

## Примеры

Показывает, как получить пользовательский идентификатор XML-данных для XML-части.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Структурированные теги документов имеют идентификаторы в форме GUID.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Смотрите также

* class [XmlMapping](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
