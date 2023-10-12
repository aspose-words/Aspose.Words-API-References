---
title: Class CustomPart
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Markup.CustomPart сорт. Представляет пользовательскую часть произвольное содержимое которая не определена стандартом ISO/IEC 29500.
type: docs
weight: 3900
url: /ru/net/aspose.words.markup/custompart/
---
## CustomPart class

Представляет пользовательскую часть (произвольное содержимое), которая не определена стандартом ISO/IEC 29500.

Чтобы узнать больше, посетите[Структурированные теги документа или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) статья документации.

```csharp
public class CustomPart
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CustomPart](custompart/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | Указывает тип содержимого этой пользовательской части. |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | Содержит данные этой пользовательской детали. |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | False, если эта пользовательская часть хранится внутри пакета OOXML. Истинно, если эта пользовательская часть является внешней целью. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Получает или задает абсолютное имя этой части в пакете OOXML или целевой URL-адрес. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Получает или задает тип связи родительской части с этой пользовательской частью. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Делает «достаточно глубокую» копию объекта. Не дублирует байты[`Data`](./data/) значение. |

### Примечания

Этот класс представляет часть OOXML, которая является целью «неизвестной связи». Все связи, не определенные в ISO/IEC 29500, считаются «неизвестными связями». Неизвестные связи разрешены в документе Office Open XML при условии, что они соответствуют рекомендациям по разметке отношений.

Microsoft Word сохраняет пользовательские части во время циклов открытия/сохранения. Некоторую дополнительную информацию можно найти здесь http://blogs.msdn.com/dmahugh/archive/2006/11/25/promptary-content-in-an-opc-package.aspx.

Aspose.Words также обрабатывает пользовательские части и, кроме того, позволяет программно получать доступ к таким частям через`CustomPart` и[`CustomPartCollection`](../custompartcollection/) объекты.

Не путайте пользовательские части с пользовательскими XML-данными. Использовать[`CustomXmlPart`](../customxmlpart/) если вам нужен для доступа к пользовательским данным XML.

### Примеры

Показывает, как получить доступ к произвольной коллекции пользовательских частей документа.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Клонируем вторую часть, затем добавляем клон в коллекцию.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Перебираем коллекцию и печатаем каждую часть.
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

// Мы можем удалять элементы из этой коллекции по отдельности или все сразу.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Смотрите также

* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)


