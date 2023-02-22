---
title: Document.PackageCustomParts
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает или задает набор настраиваемых частей произвольное содержимое которые связаны с пакетом OOXML с помощью неизвестных связей.
type: docs
weight: 290
url: /ru/net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

Получает или задает набор настраиваемых частей (произвольное содержимое), которые связаны с пакетом OOXML с помощью «неизвестных связей».

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

### Примечания

Не путайте эти настраиваемые части с пользовательскими XML-данными. Если вам нужен доступ к частям Custom XML, используйте[`CustomXmlParts`](../customxmlparts/) имущество.

Эта коллекция содержит части OOXML, родительским элементом которых является пакет OOXML, а цели имеют "неизвестную связь". Дополнительные сведения см.[`CustomPart`](../../../aspose.words.markup/custompart/).

Aspose.Words загружает и сохраняет пользовательские части только в документах OOXML.

Это свойство не может быть`нулевой`.

### Примеры

Показывает, как получить доступ к коллекции произвольных пользовательских частей документа.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Клонируем вторую часть, затем добавляем клон в коллекцию.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Перечисляем коллекцию и печатаем каждую часть.
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

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


