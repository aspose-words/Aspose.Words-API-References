---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: .NET için Aspose.Words
description: XML içeriğiniz için güvenilir bir CRC kontrol toplamıyla veri bütünlüğünü garanti altına alan CustomXmlPart DataChecksum özelliğini keşfedin. Verilerinizin güvenilirliğini artırın!
type: docs
weight: 30
url: /tr/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Döngüsel yedeklilik denetimi (CRC) toplamını belirtir[`Data`](../data/) içerik.

```csharp
public long DataChecksum { get; }
```

## Örnekler

Çalışma zamanında sağlama toplamının nasıl hesaplandığını gösterir.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// Kontrol toplamı salt okunurdur ve ilgili özel XML veri bölümünün verileri kullanılarak hesaplanır.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// Etiketin XmlPart'ını değiştirdik ve sağlama toplamı çalışma zamanında güncellendi.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Ayrıca bakınız

* class [CustomXmlPart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
