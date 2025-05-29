---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words для .NET
description: Узнайте, как свойство StructuredDocumentTagRangeStart XmlMapping связывает диапазон тегов вашего документа с пользовательскими XML-данными, улучшая интеграцию документов.
type: docs
weight: 190
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Возвращает объект, представляющий сопоставление этого структурированного диапазона тегов документа с XML-данными в пользовательской части XML текущего документа.

```csharp
public XmlMapping XmlMapping { get; }
```

## Примечания

Вы можете использовать[`SetMapping`](../../xmlmapping/setmapping/) Метод объекта this для сопоставления структурированного диапазона тегов документа с данными XML.

## Примеры

Показывает, как задать сопоставления XML для начала диапазона структурированного тега документа.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// Создаем часть XML, содержащую текст, и добавляем ее в коллекцию CustomXmlPart документа.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Создаем структурированный тег документа, который будет отображать содержимое нашего CustomXmlPart в документе.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Если мы установим сопоставление для нашего структурированного тега документа,
// он отобразит только ту часть CustomXmlPart, на которую указывает XPath.
// Этот XPath будет указывать на содержимое второго элемента "<text>" первого элемента "<root>" нашего CustomXmlPart.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Смотрите также

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
