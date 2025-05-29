---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Markup.CustomXmlPart для эффективного управления хранилищем пользовательских XML-данных в пакетах. Улучшите обработку документов сегодня!
type: docs
weight: 4610
url: /ru/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Представляет часть хранилища пользовательских XML-данных (пользовательские XML-данные в пакете).

Чтобы узнать больше, посетите[Структурированные теги документов или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) документальная статья.

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
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Указывает контрольную сумму циклического избыточного кода (CRC)[`Data`](./data/) содержание. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Возвращает или задает строку, идентифицирующую эту пользовательскую часть XML в документе OOXML. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Указывает набор схем XML, связанных с этой пользовательской частью XML. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Создает «достаточно глубокую» копию объекта. Не дублирует байты[`Data`](./data/) значение. |

## Примечания

Документ DOCX или DOC может содержать одну или несколько частей Custom XML Data Storage. Aspose.Words сохраняет и позволяет создавать и извлекать Custom XML Data через[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) коллекция.

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

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
