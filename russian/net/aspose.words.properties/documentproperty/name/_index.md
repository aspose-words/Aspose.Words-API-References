---
title: DocumentProperty.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words для .NET
description: Откройте для себя функцию DocumentProperty Name, которая легко извлекает имена свойств, улучшая управление документами и эффективность рабочего процесса.
type: docs
weight: 30
url: /ru/net/aspose.words.properties/documentproperty/name/
---
## DocumentProperty.Name property

Возвращает имя свойства.

```csharp
public string Name { get; }
```

## Примечания

Не может быть`нулевой` и не может быть пустой строкой.

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

* class [DocumentProperty](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
