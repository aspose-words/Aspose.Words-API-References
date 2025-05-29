---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: .NET için Aspose.Words
description: Belge düğüm sayfa numaralarını verimli bir şekilde hesaplamak ve belge yönetimi deneyiminizi geliştirmek için Aspose.Words.Layout.LayoutCollector sınıfını keşfedin.
type: docs
weight: 3770
url: /tr/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Bu sınıf, belge düğümlerinin sayfa numaralarının hesaplanmasına olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Sabit Sayfa Biçimine Dönüştürme](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) belgeleme makalesi.

```csharp
public class LayoutCollector
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | Bu sınıfın bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Bu toplayıcı örneğinin bağlı olduğu belgeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Toplanan tüm düzen verilerini temizler. Belge manuel olarak güncellendikten veya düzen yeniden oluşturulduktan sonra bu yöntemi çağırın. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | Düğümün bittiği sayfanın 1 tabanlı dizinini alır. Düğüm bir sayfaya eşlenemiyorsa 0 döndürür. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | Opak bir konumu döndürür[`LayoutEnumerator`](../layoutenumerator/) belirtilen düğüme karşılık gelen. Döndürülen değeri bir argüman olarak kullanabilirsiniz[`Current`](../layoutenumerator/current/) verilen belge numaralandırılmıştır ve düğümün belgesi aynıdır. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | Belirtilen düğümün kapsadığı sayfa sayısını alır. Düğüm tek bir sayfa içindeyse 0. Bu, şu şekildedir:[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | Düğümün başladığı sayfanın 1 tabanlı dizinini alır. Düğüm bir sayfaya eşlenemiyorsa 0 döndürür. |

## Notlar

Bir tane oluşturduğunuzda`LayoutCollector` ve bir tane belirtin[`Document`](../../aspose.words/document/)Eklenecek belge nesnesi, toplayıcı, belge sayfalara biçimlendirildiğinde belge düğümlerinin düzen nesnelerine eşlenmesini kaydedecektir.

Belirli bir belge düğümünün (örneğin çalıştırma, paragraf veya tablo hücresi) hangi sayfada bulunduğunu kullanarak bulabilirsiniz[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) Ve[`GetNumPagesSpanned`](./getnumpagesspanned/) yöntemler. Bu yöntemler, belgenin sayfa düzeni modelini otomatik olarak oluşturur ve gerektiğinde alanları günceller.

Artık düzen bilgilerini toplamanız gerekmediğinde, en iyisi[`Document`](./document/) mülk`hükümsüz` gereksiz yere daha fazla düzen eşlemesi toplanmasını önlemek için.

## Örnekler

Bir düğümün yayıldığı sayfa aralıklarının nasıl görüleceğini gösterir.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Belgemizin içeriğinin kaç sayfayı kapladığını saymak için "GetNumPagesSpanned" metodunu çağıralım.
// Belge boş olduğundan, sayfa sayısı şu anda sıfırdır.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Belgeyi 5 sayfalık içerikle doldur.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Düzen toplayıcısından önce, bize bir düzen sağlamak için "UpdatePageLayout" yöntemini çağırmamız gerekir.
// sayfa sayısı gibi düzenle ilgili herhangi bir metriğe ilişkin doğru bir rakam.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Herhangi bir node'un başlangıç ve bitiş sayfa numaralarını ve bunların toplam sayfa genişliklerini görebiliriz.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// LayoutEnumerator kullanarak düzen varlıkları üzerinde yineleme yapabiliriz.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator, bir ağaç gibi düzen varlıklarının koleksiyonunu dolaşabilir.
// Bunu herhangi bir düğümün karşılık gelen düzen varlığına da uygulayabiliriz.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
