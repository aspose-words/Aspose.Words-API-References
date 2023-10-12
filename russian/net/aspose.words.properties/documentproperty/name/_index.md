---
title: DocumentProperty.Name
second_title: Справочник по API Aspose.Words для .NET
description: DocumentProperty свойство. Возвращает имя свойства.
type: docs
weight: 30
url: /ru/net/aspose.words.properties/documentproperty/name/
---
## DocumentProperty.Name property

Возвращает имя свойства.

```csharp
public string Name { get; }
```

### Примечания

Не может быть`нулевой` и не может быть пустой строкой.

### Примеры

Показывает, как работать со встроенными свойствами документа.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Объект «Документ» содержит в своих членах некоторые метаданные.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Документ также хранит метаданные в своих встроенных свойствах.
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

* class [DocumentProperty](../)
* пространство имен [Aspose.Words.Properties](../../documentproperty/)
* сборка [Aspose.Words](../../../)


