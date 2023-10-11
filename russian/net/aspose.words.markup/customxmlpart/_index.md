---
title: Class CustomXmlPart
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Markup.CustomXmlPart сорт. Представляет пользовательскую часть хранилища данных XML пользовательские данные XML в пакете.
type: docs
weight: 3920
url: /ru/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Представляет пользовательскую часть хранилища данных XML (пользовательские данные XML в пакете).

Чтобы узнать больше, посетите[Структурированные теги документа или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) статья документации.

```csharp
public class CustomXmlPart
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Получает или задает XML-содержимое этой пользовательской части хранилища XML-данных. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Указывает контрольную сумму циклического избыточного кода (CRC)[`Data`](./data/) контент. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Получает или задает строку, которая идентифицирует эту пользовательскую часть XML в документе OOXML. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Указывает набор схем XML, связанных с этой пользовательской частью XML. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Делает «достаточно глубокую» копию объекта. Не дублирует байты[`Data`](./data/) значение. |

### Примечания

Документ DOCX или DOC может содержать одну или несколько частей пользовательского хранилища данных XML. Aspose.Words сохраняет, а позволяет создавать и извлекать пользовательские XML-данные с помощью[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) коллекция.

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

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)


