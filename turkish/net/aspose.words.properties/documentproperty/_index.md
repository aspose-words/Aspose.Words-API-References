---
title: Class DocumentProperty
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Properties.DocumentProperty sınıf. Özel veya yerleşik bir belge özelliğini temsil eder.
type: docs
weight: 4220
url: /tr/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

Özel veya yerleşik bir belge özelliğini temsil eder.

```csharp
public class DocumentProperty
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | Bu özelliğin içeriğe bağlı olup olmadığını gösterir. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | Bağlı bir özel belge özelliğinin kaynağını alır. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | Özelliğin adını döndürür. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | Özelliğin veri türünü alır. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | Özelliğin değerini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | Özellik değerini bool. olarak döndürür |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | Özellik değerini bayt dizisi olarak döndürür. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | Özellik değerini UTC'de DateTime olarak döndürür. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | Özellik değerini double olarak döndürür. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | Özellik değerini tamsayı olarak döndürür. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | Özellik değerini, geçerli yerel ayara göre biçimlendirilmiş bir dize olarak döndürür. |

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

* class [DocumentPropertyCollection](../documentpropertycollection/)
* ad alanı [Aspose.Words.Properties](../../aspose.words.properties/)
* toplantı [Aspose.Words](../../)


