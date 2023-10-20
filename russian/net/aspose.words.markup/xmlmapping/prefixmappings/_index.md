---
title: XmlMapping.PrefixMappings
linktitle: PrefixMappings
articleTitle: PrefixMappings
second_title: Aspose.Words для .NET
description: XmlMapping PrefixMappings свойство. Возвращает сопоставления префиксов пространства имен XML для оценкиXPath  на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.markup/xmlmapping/prefixmappings/
---
## XmlMapping.PrefixMappings property

Возвращает сопоставления префиксов пространства имен XML для оценки[`XPath`](../xpath/) .

```csharp
public string PrefixMappings { get; }
```

## Примечания

Указывает набор сопоставлений префиксов, которые будут использоваться для интерпретации выражения XPath , когда выражение XPath оценивается по пользовательским частям данных XML в документе.

## Примеры

Показывает, как настроить сопоставления XML для пользовательских частей XML.

```csharp
Document doc = new Document();

// Создайте часть XML, содержащую текст, и добавьте ее в коллекцию CustomXmlPart документа.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>", 
    Encoding.UTF8.GetString(xmlPart.Data));

// Создаем тег структурированного документа, который будет отображать содержимое нашего CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Установите сопоставление для нашего тега структурированного документа. Это отображение будет инструктировать
// наш тег структурированного документа для отображения части текстового содержимого XML-части, на которую указывает XPath.
// В данном случае это будет содержимое второго "<text>" элемент первого "<root>" элемент: «Текстовый элемент №2».
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// Добавьте в документ тег структурированного документа, чтобы отобразить содержимое нашей пользовательской части.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Смотрите также

* class [XmlMapping](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
