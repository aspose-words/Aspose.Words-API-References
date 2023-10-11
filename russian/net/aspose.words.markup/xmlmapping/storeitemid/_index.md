---
title: XmlMapping.StoreItemId
second_title: Справочник по API Aspose.Words для .NET
description: XmlMapping свойство. Указывает пользовательский идентификатор XMLданных для пользовательской части данных XML который должен использоваться для оценкиXPath выражение.
type: docs
weight: 40
url: /ru/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

Указывает пользовательский идентификатор XML-данных для пользовательской части данных XML, который должен использоваться для оценки[`XPath`](../xpath/) выражение.

```csharp
public string StoreItemId { get; }
```

### Примеры

Показывает, как получить пользовательский идентификатор данных XML части XML.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// Теги структурированных документов имеют идентификаторы в виде GUID.
StructuredDocumentTag tag = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### Смотрите также

* class [XmlMapping](../)
* пространство имен [Aspose.Words.Markup](../../xmlmapping/)
* сборка [Aspose.Words](../../../)


