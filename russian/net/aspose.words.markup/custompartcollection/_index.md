---
title: CustomPartCollection Class
linktitle: CustomPartCollection
articleTitle: CustomPartCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.Markup.CustomPartCollection сорт. Представляет коллекциюCustomPart объекты на С#.
type: docs
weight: 3910
url: /ru/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

Представляет коллекцию[`CustomPart`](../custompart/) объекты.

Чтобы узнать больше, посетите[Структурированные теги документа или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) статья документации.

```csharp
public class CustomPartCollection : IEnumerable<CustomPart>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CustomPartCollection](custompartcollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | Получает или задает элемент по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(*[CustomPart](../custompart/)*) | Добавляет элемент в коллекцию. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | Удаляет все элементы из коллекции. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | Создает глубокую копию этой коллекции и ее элементов. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов коллекции. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(*int*) | Удаляет элемент по указанному индексу. |

## Примечания

Обычно вам не нужно создавать экземпляры этого класса. Вы получаете доступ к пользовательским частям , связанным с пакетом OOXML, через[`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) свойство.

## Примеры

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

* class [CustomPart](../custompart/)
* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
