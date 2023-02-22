---
title: Document.ExtractPages
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. Document belirtilen sayfa aralığını temsil eden nesne.
type: docs
weight: 580
url: /tr/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

[`Document`](../) belirtilen sayfa aralığını temsil eden nesne.

```csharp
public Document ExtractPages(int index, int count)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Ayıklanacak ilk sayfanın sıfır tabanlı dizini. |
| count | Int32 | Çıkarılacak sayfa sayısı. |

### Notlar

Ortaya çıkan belge, 'Belirli sayfaları yazdır' işlemini gerçekleştirmişiz gibi MS Word'dekine benzemelidir – numaralandırma, üstbilgiler/altbilgiler ve çapraz tablolar düzeni korunacaktır. Ancak çok sayıda nüans nedeniyle, sayfa sayısını azaltırken, mizanpajın tam eşleşmesi, çok fazla çaba gerektiren sessiz ve karmaşık bir iştir. Belge karmaşıklığına bağlı olarak, kaynak belgeyle karşılaştırıldığında ortaya çıkan belge içeriği düzeninde küçük farklılıklar olabilir. çok takdir edilecektir.

### Örnekler

Belgeden belirtilen sayfa aralığının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


