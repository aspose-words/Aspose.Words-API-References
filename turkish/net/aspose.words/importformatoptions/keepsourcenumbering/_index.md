---
title: ImportFormatOptions.KeepSourceNumbering
second_title: Aspose.Words for .NET API Referansı
description: ImportFormatOptions mülk. Kaynak ve hedef belgelerde çakıştığında numaralandırmanın nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ .
type: docs
weight: 60
url: /tr/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Kaynak ve hedef belgelerde çakıştığında numaralandırmanın nasıl içe aktarılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

### Örnekler

Aynı liste tanımı tanımlayıcısına sahip listeleri içe aktarırken çakışmanın nasıl çözüleceğini gösterir.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Farklı bir liste tanımı kimliği uygulamak için "KeepSourceNumbering" özelliğini "true" olarak ayarlayın
// Aspose.Words'ün bunları hedef belgelere aktarmasıyla aynı stillere.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Numaralandırılmış listelerle bir belgenin nasıl içe aktarılacağını gösterir.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// Liste stilleri arasında çakışma varsa kaynak belgenin liste formatını uygulayın.
// Liste numaralarını hedef belgeye aktarmamak için "KeepSourceNumbering" özelliğini "false" olarak ayarlayın.
// "KeepSourceNumbering" özelliğini "true" olarak ayarlayarak tüm çakışmaları içe aktarın
// kaynak belgedekiyle aynı görünüme sahip stil numaralandırmasını listeleyin.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Kaynak ve hedef belgelerdeki liste numaralandırma çakışmalarının nasıl çözüleceğini gösterir.

```csharp
// Özel liste numaralandırma şemasına sahip bir belge açın ve ardından kopyalayın.
// Her ikisi de aynı numaralandırma formatına sahip olduğundan, bir belgeyi diğerine aktarırsak formatlar çakışacaktır.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Belgenin klonunu orijinale aktarıp eklediğimizde,
// aynı liste formatına sahip iki liste birleşecek.
// "KeepSourceNumbering" bayrağını "false" olarak ayarlarsak, belge klonundaki liste
// orijinale eklediğimiz, eklediğimiz listenin numaralandırmasını taşıyacaktır.
// Bu, iki listeyi etkili bir şekilde tek bir listede birleştirecektir.
// "KeepSourceNumbering" bayrağını "true" olarak ayarlarsak belge klonu
 // liste orijinal numaralandırmasını koruyacak ve iki listenin ayrı listeler olarak görünmesini sağlayacaktır.
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
* ad alanı [Aspose.Words](../../importformatoptions/)
* toplantı [Aspose.Words](../../../)


