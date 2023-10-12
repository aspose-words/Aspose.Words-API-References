---
title: XmlMapping.SetMapping
second_title: Справочник по API Aspose.Words для .NET
description: XmlMapping метод. Устанавливает сопоставление между тегом родительского структурированного документа и узлом XML пользовательской части данных XML.
type: docs
weight: 70
url: /ru/net/aspose.words.markup/xmlmapping/setmapping/
---
## XmlMapping.SetMapping method

Устанавливает сопоставление между тегом родительского структурированного документа и узлом XML пользовательской части данных XML.

```csharp
public bool SetMapping(CustomXmlPart customXmlPart, string xPath, string prefixMapping)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| customXmlPart | CustomXmlPart | Пользовательская часть данных XML для сопоставления. |
| xPath | String | Выражение XPath для поиска узла XML. |
| prefixMapping | String | Сопоставления префиксов пространства имен XML для оценки XPath. |

### Возвращаемое значение

Флаг, указывающий, успешно ли сопоставлен тег родительского структурированного документа с узлом XML.

### Примеры

Показывает, как создать тег структурированного документа с пользовательскими данными XML.

```csharp
Document doc = new Document();

// Создаем часть XML, содержащую данные, и добавляем ее в коллекцию документа.
// Если мы включим вкладку «Разработчик» в Microsoft Word,
// мы можем найти элементы из этой коллекции в «Панели сопоставления XML» вместе с несколькими элементами по умолчанию.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Ниже приведены два способа обращения к частям XML.
// 1 - По индексу в пользовательской коллекции частей XML:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - По GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Добавляем ассоциацию схемы XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Клонируем часть и затем вставляем ее в коллекцию.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Перебираем коллекцию и печатаем содержимое каждой части.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Используйте метод «RemoveAt», чтобы удалить клонированную часть по индексу.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Клонировать коллекцию частей XML, а затем использовать метод «Очистить», чтобы удалить сразу все ее элементы.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Создаем структурированный тег документа, который будет отображать содержимое нашей части, и вставляем его в тело документа.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Смотрите также

* class [CustomXmlPart](../../customxmlpart/)
* class [XmlMapping](../)
* пространство имен [Aspose.Words.Markup](../../xmlmapping/)
* сборка [Aspose.Words](../../../)


