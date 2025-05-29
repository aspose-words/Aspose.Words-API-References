---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: .NET için Aspose.Words
description: TxtLoadOptions'ın DetectNumberingWithWhitespaces özelliğiyle belge içe aktarımlarınızı optimize edin ve düz metinden numaralı listelerin doğru bir şekilde tanınmasını sağlayın.
type: docs
weight: 40
url: /tr/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Belge düz metin biçiminden içe aktarıldığında numaralı liste öğelerinin nasıl tanınacağını belirtmeye olanak tanır. Varsayılan değer`doğru`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## Notlar

Bu seçenek şu şekilde ayarlanırsa:`YANLIŞ`, liste tanıma algoritması, liste numaraları nokta, sağ parantez veya madde işareti sembollerinden (örneğin "•", "*", "-" veya "o") biriyle bittiğinde liste paragraflarını algılar.

Bu seçenek şu şekilde ayarlanırsa:`doğru`, boşluklar aynı zamanda liste numarası sınırlayıcıları olarak da kullanılır: Arapça stil numaralandırma için liste tanıma algoritması (1., 1.1.2.) hem boşlukları hem de nokta (".") sembollerini kullanır.

## Örnekler

Düz metin belgeleri yüklenirken listelerin nasıl algılanacağını gösterir.

```csharp
// Dört ayrı parçadan oluşan bir dizgede düz metin belgesi oluşturun; bu parçaları liste olarak yorumlayabiliriz.
// farklı ayırıcılarla. Düz metin belgesini bir "Belge" nesnesine yüklerken,
// Aspose.Words her zaman ilk üç listeyi algılayacak ve bir "Liste" nesnesi ekleyecektir
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

// Bir belgenin oluşturucusuna geçirebileceğimiz bir "TxtLoadOptions" nesnesi oluşturun
// düz metin belgenin nasıl yükleneceğini değiştirmek için.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Numaralandırılmış öğeleri algılamak için "DetectNumberingWithWhitespaces" özelliğini "true" olarak ayarlayın
// boşluk ayraçlarıyla, örneğin belgedeki dördüncü liste gibi, listeler olarak.
// Bu ayrıca sayılarla başlayan paragrafların liste olarak yanlış algılanmasına da neden olabilir.
// "DetectNumberingWithWhitespaces" özelliğini "false" olarak ayarlayın
// numaralandırılmış öğelerden boşluk ayraçlarıyla liste oluşturulmaması.
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
