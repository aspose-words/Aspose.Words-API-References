---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: Aspose.Words for .NET
description: TxtLoadOptions DetectNumberingWithWhitespaces mülk. Belge düz metin biçiminden içe aktarıldığında numaralı liste öğelerinin nasıl tanınacağını belirlemeye olanak tanır. Varsayılan değerdoğru C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Belge düz metin biçiminden içe aktarıldığında numaralı liste öğelerinin nasıl tanınacağını belirlemeye olanak tanır. Varsayılan değer:`doğru`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## Notlar

Bu seçenek olarak ayarlanmışsa`YANLIŞ`, liste tanıma algoritması, liste numaraları nokta, sağ köşeli parantez veya madde işareti simgeleriyle ("•", "*", "-" veya "o" gibi) ile bittiğinde liste paragraflarını algılar.

Bu seçenek olarak ayarlanmışsa`doğru`boşluklar aynı zamanda liste numarası sınırlayıcıları olarak da kullanılır: Arapça stil numaralandırma için liste tanıma algoritması (1., 1.1.2.) hem boşlukları hem de nokta (".") sembollerini kullanır.

## Örnekler

Düz metin belgeleri yüklenirken listelerin nasıl algılanacağını gösterir.

```csharp
// Liste olarak yorumlayabileceğimiz dört ayrı bölümden oluşan bir dizede düz metin belgesi oluşturun,
// farklı sınırlayıcılarla. Düz metin belgesini bir "Belge" nesnesine yükledikten sonra,
// Aspose.Words her zaman ilk üç listeyi algılayacak ve bir "List" nesnesi ekleyecektir
// her biri için belgenin "Listeler" özelliğine.
const string textDoc = "Full stop delimiters:\n" +
                       "1. First list item 1\n" +
                       "2. First list item 2\n" +
                       "3. First list item 3\n\n" +
                       "Right bracket delimiters:\n" +
                       "1) Second list item 1\n" +
                       "2) Second list item 2\n" +
                       "3) Second list item 3\n\n" +
                       "Bullet delimiters:\n" +
                       "• Third list item 1\n" +
                       "• Third list item 2\n" +
                       "• Third list item 3\n\n" +
                       "Whitespace delimiters:\n" +
                       "1 Fourth list item 1\n" +
                       "2 Fourth list item 2\n" +
                       "3 Fourth list item 3";

// Bir belgenin yapıcısına iletebileceğimiz bir "TxtLoadOptions" nesnesi oluşturun
// düz metin belgesini yükleme şeklimizi değiştirmek için.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Numaralı öğeleri algılamak için "DetectNumberingWithWhitespaces" özelliğini "true" olarak ayarlayın
// belgemizdeki dördüncü liste gibi boşluk sınırlayıcılarla listeler halinde.
// Bu aynı zamanda sayılarla başlayan paragrafların liste olarak yanlış algılanmasına da neden olabilir.
// "DetectNumberingWithWhitespaces" özelliğini "false" olarak ayarlayın
// boşluk sınırlayıcıları olan numaralandırılmış öğelerden listeler oluşturmamak için.
loadOptions.DetectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    Assert.AreEqual(4, doc.Lists.Count);
    Assert.True(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
else
{
    Assert.AreEqual(3, doc.Lists.Count);
    Assert.False(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
```

### Ayrıca bakınız

* class [TxtLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
