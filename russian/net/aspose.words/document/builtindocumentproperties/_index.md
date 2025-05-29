---
title: Document.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: Aspose.Words для .NET
description: Изучите свойство BuiltInDocumentProperties, чтобы получить доступ к основным свойствам документа, что улучшит управление документами и повысит эффективность.
type: docs
weight: 50
url: /ru/net/aspose.words/document/builtindocumentproperties/
---
## Document.BuiltInDocumentProperties property

Возвращает коллекцию, которая представляет все встроенные свойства документа.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

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

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
