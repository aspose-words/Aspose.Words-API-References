---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words для .NET
description: Aspose.Words.Markup.XmlMapping сорт. Указывает информацию которая используется для установления сопоставления между тегом структурированного документа Parent и элементом XML хранящимся в пользовательской части данных XML в документе на С#.
type: docs
weight: 4100
url: /ru/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Указывает информацию, которая используется для установления сопоставления между тегом структурированного документа Parent и элементом XML, хранящимся в пользовательской части данных XML в документе.

Чтобы узнать больше, посетите[Структурированные теги документа или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) статья документации.

```csharp
public class XmlMapping
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Возвращает пользовательскую часть данных XML, с которой сопоставлен тег родительского структурированного документа. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Возвращает`истинный` если тег родительского структурированного документа успешно сопоставлен с данными XML. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Возвращает сопоставления префиксов пространства имен XML для оценки[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Указывает пользовательский идентификатор XML-данных для пользовательской части данных XML, который должен использоваться для оценки[`XPath`](./xpath/) выражение. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Возвращает выражение XPath, которое оценивается для поиска пользовательского узла XML , сопоставленного с тегом родительского структурированного документа. |

## Методы

| Имя | Описание |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Удаляет сопоставление родительского структурированного документа с данными XML. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Устанавливает сопоставление между тегом родительского структурированного документа и узлом XML пользовательской части данных XML. |

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

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
