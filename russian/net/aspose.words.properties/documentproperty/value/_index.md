---
title: DocumentProperty.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words для .NET
description: Узнайте, как эффективно управлять значениями DocumentProperty — легко извлекайте и обновляйте значения свойств для улучшенного контроля над документами и повышения производительности.
type: docs
weight: 50
url: /ru/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

Получает или задает значение свойства.

```csharp
public object Value { get; set; }
```

## Примечания

Не может быть`нулевой`.

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
