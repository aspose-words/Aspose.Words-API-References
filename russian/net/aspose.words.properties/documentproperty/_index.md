---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Properties.DocumentProperty для эффективного управления пользовательскими и встроенными свойствами документа. Улучшите обработку документов сегодня!
type: docs
weight: 5200
url: /ru/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

Представляет пользовательское или встроенное свойство документа.

Чтобы узнать больше, посетите[Работа со свойствами документа](https://docs.aspose.com/words/net/work-with-document-properties/) документальная статья.

```csharp
public class DocumentProperty
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | Показывает, связано ли это свойство с содержимым или нет. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | Получает источник связанного пользовательского свойства документа. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | Возвращает имя свойства. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | Получает тип данных свойства. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | Получает или задает значение свойства. |

## Методы

| Имя | Описание |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | Возвращает значение свойства как bool. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | Возвращает значение свойства в виде массива байтов. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | Возвращает значение свойства как**ДатаВремя** в UTC. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | Возвращает значение свойства как double. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | Возвращает значение свойства как целое число. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | Возвращает значение свойства в виде строки, отформатированной в соответствии с текущей локалью. |

## Примеры

Показывает, как работать со встроенными свойствами документа.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Объект «Документ» содержит некоторые метаданные в своих членах.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Документ также хранит метаданные во встроенных свойствах.
// Каждое встроенное свойство является членом объекта «BuiltInDocumentProperties» документа.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Некоторые свойства могут хранить несколько значений.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### Смотрите также

* class [DocumentPropertyCollection](../documentpropertycollection/)
* пространство имен [Aspose.Words.Properties](../../aspose.words.properties/)
* сборка [Aspose.Words](../../)
