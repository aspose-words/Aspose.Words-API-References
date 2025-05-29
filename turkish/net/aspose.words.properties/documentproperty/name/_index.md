---
title: DocumentProperty.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: Belge yönetiminizi ve iş akışı verimliliğinizi artırarak özellik adlarını zahmetsizce getiren DocumentProperty Name özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.properties/documentproperty/name/
---
## DocumentProperty.Name property

Özelliğin adını döndürür.

```csharp
public string Name { get; }
```

## Notlar

Olamaz`hükümsüz` ve boş bir dize olamaz.

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

* class [DocumentProperty](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
