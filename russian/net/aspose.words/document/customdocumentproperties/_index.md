---
title: Document.CustomDocumentProperties
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Возвращает коллекцию которая представляет все пользовательские свойства документа.
type: docs
weight: 70
url: /ru/net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

Возвращает коллекцию, которая представляет все пользовательские свойства документа.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

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

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


