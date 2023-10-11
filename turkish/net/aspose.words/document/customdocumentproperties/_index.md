---
title: Document.CustomDocumentProperties
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. Belgenin tüm özel belge özelliklerini temsil eden bir koleksiyon döndürür.
type: docs
weight: 70
url: /tr/net/aspose.words/document/customdocumentproperties/
---
## Document.CustomDocumentProperties property

Belgenin tüm özel belge özelliklerini temsil eden bir koleksiyon döndürür.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

### Örnekler

Yerleşik belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// "Belge" nesnesi, meta verilerinin bir kısmını üyelerinde içerir.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Belge aynı zamanda meta verileri yerleşik özelliklerinde de saklar.
// Her yerleşik özellik, belgenin "BuiltInDocumentProperties" nesnesinin bir üyesidir.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Bazı özellikler birden fazla değer saklayabilir.
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

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


