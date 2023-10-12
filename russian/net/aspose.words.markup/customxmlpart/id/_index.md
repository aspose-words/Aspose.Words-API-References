---
title: CustomXmlPart.Id
second_title: Справочник по API Aspose.Words для .NET
description: CustomXmlPart свойство. Получает или задает строку которая идентифицирует эту пользовательскую часть XML в документе OOXML.
type: docs
weight: 40
url: /ru/net/aspose.words.markup/customxmlpart/id/
---
## CustomXmlPart.Id property

Получает или задает строку, которая идентифицирует эту пользовательскую часть XML в документе OOXML.

```csharp
public string Id { get; set; }
```

### Примечания

ISO/IEC 29500 указывает, что это значение является GUID, но старые версии Microsoft Word допускали здесь любую строку . Aspose.Words делает то же самое для формата ECMA-376. Но учтите, что Microsoft Word Online не может открыть документ, созданный со значением, отличным от GUID. Таким образом, предпочтительным значением для этого свойства является GUID.

Допустимое значение должно быть идентификатором, уникальным среди всех пользовательских частей данных XML в этом документе.

Значение по умолчанию — пустая строка. Значение не может быть`нулевой`.

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

* class [CustomXmlPart](../)
* пространство имен [Aspose.Words.Markup](../../customxmlpart/)
* сборка [Aspose.Words](../../../)


