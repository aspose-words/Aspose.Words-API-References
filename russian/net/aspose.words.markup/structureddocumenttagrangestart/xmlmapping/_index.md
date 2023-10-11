---
title: StructuredDocumentTagRangeStart.XmlMapping
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTagRangeStart свойство. Получает объект который представляет сопоставление диапазона тегов структурированного документа с XMLданными в пользовательской XMLчасти текущего документа.
type: docs
weight: 180
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Получает объект, который представляет сопоставление диапазона тегов структурированного документа с XML-данными в пользовательской XML-части текущего документа.

```csharp
public XmlMapping XmlMapping { get; }
```

### Примечания

Вы можете использовать[`SetMapping`](../../xmlmapping/setmapping/) метод объекта this для сопоставления диапазона тегов структурированного документа с данными XML.

### Примеры

Показывает, как настроить сопоставления XML для начала диапазона тега структурированного документа.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// Создайте часть XML, содержащую текст, и добавьте ее в коллекцию CustomXmlPart документа.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Создаем структурированный тег документа, который будет отображать содержимое нашей CustomXmlPart в документе.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Если мы установим сопоставление для нашего тега структурированного документа,
// будет отображаться только часть CustomXmlPart, на которую указывает XPath.
// Этот XPath будет указывать на второй "<text>" содержимого. элемент первого "<root>" элемент нашего CustomXmlPart.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Смотрите также

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* сборка [Aspose.Words](../../../)


