---
title: XmlMapping.IsMapped
linktitle: IsMapped
articleTitle: IsMapped
second_title: Aspose.Words для .NET
description: Узнайте, как свойство XmlMapping IsMapped эффективно проверяет сопоставление XML-данных для структурированных документов, обеспечивая бесшовную интеграцию и точность.
type: docs
weight: 20
url: /ru/net/aspose.words.markup/xmlmapping/ismapped/
---
## XmlMapping.IsMapped property

Возврат`истинный` если родительский структурированный тег документа успешно сопоставлен с XML-данными.

```csharp
public bool IsMapped { get; }
```

## Примеры

Показывает, как устанавливать XML-сопоставления для пользовательских XML-частей.

```csharp
Document doc = new Document();

// Создаем часть XML, содержащую текст, и добавляем ее в коллекцию CustomXmlPart документа.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Создаем структурированный тег документа, который будет отображать содержимое нашего CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Установите сопоставление для нашего структурированного тега документа. Это сопоставление будет указывать
// наш структурированный тег документа для отображения части текстового содержимого XML-части, на которую указывает XPath.
// В этом случае это будет содержимое второго элемента "<text>" первого элемента "<root>": "Текстовый элемент №2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", тег.XmlMapping.PrefixMappings);

// Добавляем структурированный тег документа в документ для отображения содержимого из нашей пользовательской части.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Смотрите также

* class [XmlMapping](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
