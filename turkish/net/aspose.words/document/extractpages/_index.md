---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words for .NET
description: Document ExtractPages yöntem. Şunu döndürürDocument belirtilen sayfa aralığını temsil eden nesne C#'da.
type: docs
weight: 600
url: /tr/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Şunu döndürür:[`Document`](../) belirtilen sayfa aralığını temsil eden nesne.

```csharp
public Document ExtractPages(int index, int count)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Çıkarılacak ilk sayfanın sıfır tabanlı dizini. |
| count | Int32 | Çıkarılacak sayfa sayısı. |

## Notlar

Ortaya çıkan belge, sanki 'Belirli sayfaları yazdır' işlemini gerçekleştirmişiz gibi MS Word'dekine benzemelidir - numaralandırma, üstbilgiler/altbilgiler ve çapraz tablo düzeni korunacaktır. Ancak çok sayıda nüans nedeniyle, görünen sayfa sayısını azaltırken mizanpajın tam olarak eşleştirilmesi, oldukça fazla çaba gerektiren, oldukça karmaşık bir iştir. Belgenin karmaşıklığına bağlı olarak, ortaya çıkan belge içeriği düzeninde, kaynak belgeyle karşılaştırıldığında küçük farklılıklar olabilir. Herhangi bir geri bildirim, çok takdir ediyorum.

## Örnekler

Belgeden belirli aralıktaki sayfaların nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
