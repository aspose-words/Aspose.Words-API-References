---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: .NET için Aspose.Words
description: Özel ve yerleşik belge özelliklerini verimli bir şekilde yönetmek için Aspose.Words.Properties.DocumentProperty sınıfını keşfedin. Belge işlemenizi bugün geliştirin!
type: docs
weight: 5200
url: /tr/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

Özel veya yerleşik bir belge özelliğini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belge Özellikleriyle Çalışma](https://docs.aspose.com/words/net/work-with-document-properties/) belgeleme makalesi.

```csharp
public class DocumentProperty
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | Bu özelliğin içeriğe bağlı olup olmadığını gösterir. |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | Bağlantılı özel belge özelliğinin kaynağını alır. |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | Özelliğin adını döndürür. |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | Özelliğin veri türünü alır. |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | Özelliğin değerini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | Özellik değerini bool olarak döndürür. |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | Özellik değerini bayt dizisi olarak döndürür. |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | Özellik değerini şu şekilde döndürür:**TarihSaat** UTC'de. |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | Özellik değerini double olarak döndürür. |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | Özellik değerini tam sayı olarak döndürür. |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | Özellik değerini geçerli yerel ayarlara göre biçimlendirilmiş bir dize olarak döndürür. |

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

* class [DocumentPropertyCollection](../documentpropertycollection/)
* ad alanı [Aspose.Words.Properties](../../aspose.words.properties/)
* toplantı [Aspose.Words](../../)
