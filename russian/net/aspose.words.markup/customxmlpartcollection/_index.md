---
title: Class CustomXmlPartCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Markup.CustomXmlPartCollection сорт. Представляет коллекцию пользовательских частей XML. ПредметыCustomXmlPart объекты.
type: docs
weight: 3930
url: /ru/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

Представляет коллекцию пользовательских частей XML. Предметы[`CustomXmlPart`](../customxmlpart/) объекты.

Чтобы узнать больше, посетите[Структурированные теги документа или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) статья документации.

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | Получает или задает элемент по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(CustomXmlPart) | Добавляет элемент в коллекцию. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(string, string) | Создает новую часть XML с указанным XML и добавляет ее в коллекцию. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | Удаляет все элементы из коллекции. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | Создает глубокую копию этой коллекции и ее элементов. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(string) | Находит и возвращает пользовательскую часть XML по ее идентификатору. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов коллекции. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(int) | Удаляет элемент по указанному индексу. |

### Примечания

Обычно вам не нужно создавать экземпляры этого класса. Вы можете получить доступ к пользовательским XML-данным , хранящимся в документе, через[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) свойство.

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

* class [CustomXmlPart](../customxmlpart/)
* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)


