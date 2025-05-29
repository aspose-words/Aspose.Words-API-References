---
title: IStructuredDocumentTag.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words для .NET
description: Узнайте, как свойство IStructuredDocumentTag XmlMapping связывает структурированные теги с XML-данными, улучшая настройку и интеграцию документов.
type: docs
weight: 160
url: /ru/net/aspose.words.markup/istructureddocumenttag/xmlmapping/
---
## IStructuredDocumentTag.XmlMapping property

Получает объект, представляющий сопоставление этого структурированного тега документа с XML-данными в пользовательской XML-части текущего документа.

```csharp
public XmlMapping XmlMapping { get; }
```

## Примечания

Вы можете использовать[`SetMapping`](../../xmlmapping/setmapping/)метод этого объекта для сопоставления структурированного тега документа с данными XML.

## Примеры

Показывает, как создать структурированный тег документа с пользовательскими XML-данными.

```csharp
Document doc = new Document();

// Создаем часть XML, содержащую данные, и добавляем ее в коллекцию документа.
// Если мы включим вкладку «Разработчик» в Microsoft Word,
// мы можем найти элементы из этой коллекции в «Панели сопоставления XML», а также несколько элементов по умолчанию.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Ниже приведены два способа ссылки на части XML.
// 1 — По индексу в коллекции пользовательских частей XML:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - По GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Добавить ассоциацию схемы XML.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Клонируем часть, а затем вставляем ее в коллекцию.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Проходим по коллекции и выводим содержимое каждой части.
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

// Используйте метод «RemoveAt» для удаления клонированной части по индексу.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Клонируем коллекцию частей XML, а затем используем метод «Очистить», чтобы удалить все ее элементы одновременно.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Создаем структурированный тег документа, который будет отображать содержимое нашей части, и вставляем его в тело документа.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Смотрите также

* class [XmlMapping](../../xmlmapping/)
* interface [IStructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
