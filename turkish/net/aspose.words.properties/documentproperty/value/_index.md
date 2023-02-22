---
title: DocumentProperty.Value
second_title: Aspose.Words for .NET API Referansı
description: DocumentProperty mülk. Özelliğin değerini alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.properties/documentproperty/value/
---
## DocumentProperty.Value property

Özelliğin değerini alır veya ayarlar.

```csharp
public object Value { get; set; }
```

### Notlar

Boş olamaz.

### Örnekler

Yerleşik belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// "Belge" nesnesi, meta verilerinin bir kısmını üyelerinde içerir.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Belge ayrıca meta verileri yerleşik özelliklerinde de saklar.
// Her yerleşik özellik, belgenin "BuiltInDocumentProperties" nesnesinin bir üyesidir.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Bazı özellikler birden fazla değer depolayabilir.
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

* class [DocumentProperty](../)
* ad alanı [Aspose.Words.Properties](../../documentproperty/)
* toplantı [Aspose.Words](../../../)


