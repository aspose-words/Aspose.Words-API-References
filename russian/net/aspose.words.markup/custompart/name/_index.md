---
title: CustomPart.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words для .NET
description: Узнайте, как управлять именами CustomPart в пакетах OOXML. Легко устанавливайте или извлекайте абсолютные имена для бесшовной интеграции и улучшенной функциональности.
type: docs
weight: 50
url: /ru/net/aspose.words.markup/custompart/name/
---
## CustomPart.Name property

Возвращает или задает абсолютное имя этой части в пакете OOXML или целевом URL.

```csharp
public string Name { get; set; }
```

## Примечания

Если цель отношения является внутренней, то это свойство является абсолютным именем части в пакете. Если цель отношения является внешней, то это свойство является целевым URL.

Значение по умолчанию — пустая строка. Допустимое значение должно быть непустой строкой.

## Примеры

Показывает, как получить доступ к коллекции произвольных пользовательских частей документа.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Клонируем вторую часть, затем добавляем клон в коллекцию.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Перечислить коллекцию и вывести каждую часть.
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

// Мы можем удалить элементы из этой коллекции по отдельности или все сразу.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Смотрите также

* class [CustomPart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
