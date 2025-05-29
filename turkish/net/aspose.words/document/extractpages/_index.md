---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: .NET için Aspose.Words
description: Belirli sayfa aralıklarını zahmetsizce almak, belge yönetiminizi ve verimliliğinizi artırmak için Document ExtractPages yöntemini keşfedin.
type: docs
weight: 640
url: /tr/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

şunu döndürür:[`Document`](../) belirtilen sayfa aralığını temsil eden nesne.

```csharp
public Document ExtractPages(int index, int count)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Çıkarılacak ilk sayfanın sıfır tabanlı indeksi. |
| count | Int32 | Çıkarılacak sayfa sayısı. |

## Notlar

Sonuçta ortaya çıkan belge, 'Belirli sayfaları yazdır' işlemini gerçekleştirmişiz gibi MS Word'deki gibi görünmelidir; numaralandırma, başlıklar/altbilgiler ve çapraz tablo düzeni korunacaktır. Ancak sayfa sayısını azaltırken ortaya çıkan çok sayıda nüans nedeniyle, düzenin tam olarak eşleşmesi oldukça karmaşık bir iştir ve çok fazla çaba gerektirir. Belgenin karmaşıklığına bağlı olarak, sonuçta ortaya çıkan belge içeriği düzeninde kaynak belgeye kıyasla küçük farklılıklar olabilir. Her türlü geri bildirim büyük bir memnuniyetle karşılanacaktır.

## Örnekler

Belgeden belirtilen sayfa aralığının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
