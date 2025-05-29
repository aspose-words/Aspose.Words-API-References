---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Markup.XmlMapping, который позволяет легко связать структурированные теги документа с элементами XML, улучшая интеграцию данных вашего документа.
type: docs
weight: 4790
url: /ru/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Указывает информацию, которая используется для установления сопоставления между структурированным тегом документа parent и элементом XML, хранящимся в пользовательской части данных XML в документе.

Чтобы узнать больше, посетите[Структурированные теги документов или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) документальная статья.

```csharp
public class XmlMapping
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Возвращает пользовательскую часть данных XML, с которой сопоставляется родительский структурированный тег документа. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Возврат`истинный` если родительский структурированный тег документа успешно сопоставлен с XML-данными. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Возвращает сопоставления префиксов пространства имен XML для оценки[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Указывает пользовательский идентификатор данных XML для пользовательской части данных XML, которая будет использоваться для оценки[`XPath`](./xpath/) выражение. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Возвращает выражение XPath, которое вычисляется для поиска пользовательского XML-узла , сопоставленного с родительским структурированным тегом документа. |

## Методы

| Имя | Описание |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Удаляет сопоставление родительского структурированного документа с данными XML. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Устанавливает сопоставление между родительским структурированным тегом документа и узлом XML пользовательской части данных XML. |

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

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
