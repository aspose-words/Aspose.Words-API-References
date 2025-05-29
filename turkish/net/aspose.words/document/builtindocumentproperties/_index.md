---
title: Document.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: .NET için Aspose.Words
description: Belge yönetiminizi ve verimliliğinizi artırmak için temel belge özelliklerine erişmek üzere BuiltInDocumentProperties özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/document/builtindocumentproperties/
---
## Document.BuiltInDocumentProperties property

Belgenin tüm yerleşik belge özelliklerini temsil eden bir koleksiyon döndürür.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

## Örnekler

Yerleşik belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// "Belge" nesnesi üyelerinde bazı meta verilerini barındırır.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Belge aynı zamanda yerleşik özelliklerinde meta verileri de depolar.
// Her yerleşik özellik, belgenin "BuiltInDocumentProperties" nesnesinin bir üyesidir.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Bazı özellikler birden fazla değeri depolayabilir.
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

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
