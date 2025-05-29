---
title: ImportFormatOptions.KeepSourceNumbering
linktitle: KeepSourceNumbering
articleTitle: KeepSourceNumbering
second_title: .NET için Aspose.Words
description: ImportFormatOptions KeepSourceNumbering özelliğiyle belge numaralandırmasını kontrol edin. Sorunsuz içe aktarımlar için çakışmaları kolayca yönetin. Varsayılan, false.
type: docs
weight: 60
url: /tr/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Kaynak ve hedef belgelerde çakışma olduğunda numaralandırmanın nasıl içe aktarılacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

## Örnekler

Aynı liste tanımlama tanımlayıcısına sahip listeleri içe aktarırken bir çakışmanın nasıl çözüleceğini gösterir.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Farklı bir liste tanımı kimliği uygulamak için "KeepSourceNumbering" özelliğini "true" olarak ayarlayın
// Aspose.Words ile aynı stilleri hedef belgelere aktarır.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Numaralandırılmış listeler içeren bir belgenin nasıl içe aktarılacağını gösterir.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// Liste stilleri arasında bir çakışma varsa, kaynak belgenin liste biçimini uygula.
// Hedef belgeye herhangi bir liste numarası aktarılmaması için "KeepSourceNumbering" özelliğini "false" olarak ayarlayın.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayın, tüm çakışanları içe aktarın
// kaynak belgedeki görünümüyle aynı olan liste stili numaralandırma.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Kaynak ve hedef belgelerdeki liste numaralandırma çakışmalarının nasıl çözüleceğini gösterir.

```csharp
// Özel liste numaralandırma şemasına sahip bir belge açın ve ardından onu kopyalayın.
// Her ikisinin de numaralandırma biçimi aynı olduğundan, bir belgeyi diğerine aktardığımızda biçimler çakışacaktır.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Belgenin klonunu orijinaline aktardığımızda ve sonra eklediğimizde,
// daha sonra aynı liste formatına sahip iki liste birleşecektir.
// "KeepSourceNumbering" bayrağını "false" olarak ayarlarsak, belge klonundan gelen liste
// orijinaline eklediğimiz her bir liste, onu eklediğimiz listenin numaralandırmasını sürdürecektir.
// Bu, iki listeyi etkili bir şekilde birleştirecektir.
// "KeepSourceNumbering" bayrağını "true" olarak ayarlarsak, belge klonu
 // liste orijinal numaralandırmasını koruyarak iki listenin ayrı listeler olarak görünmesini sağlar.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
