---
title: DocumentProperty.ToString
linktitle: ToString
articleTitle: ToString
second_title: .NET için Aspose.Words
description: Yerel ayarlara göre özellik değerlerini dizeler halinde biçimlendiren, veri sunumunu ve kullanıcı deneyimini geliştiren DocumentProperty ToString yöntemini keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

Özellik değerini geçerli yerel ayarlara göre biçimlendirilmiş bir dize olarak döndürür.

```csharp
public override string ToString()
```

## Notlar

Bir boolean özelliğini "Y" veya "N"ye dönüştürür. Bir tarih özelliğini kısa bir tarih dizesine dönüştürür. Diğer tüm türler için bir özelliği Object.ToString() kullanarak dönüştürür.

## Örnekler

Özel belge özelliklerinin çeşitli tür dönüştürme yöntemlerini gösterir.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

Özel belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Her belge, yerleşik özellikler gibi anahtar-değer çiftleri olan bir dizi özel özellik içerir.
 // Belgenin yerleşik özelliklerin sabit bir listesi vardır. Kullanıcı tüm özel özellikleri oluşturur.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Ayrıca bakınız

* class [DocumentProperty](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
