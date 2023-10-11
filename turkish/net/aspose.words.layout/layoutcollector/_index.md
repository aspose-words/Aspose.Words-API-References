---
title: Class LayoutCollector
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Layout.LayoutCollector sınıf. Bu sınıf belge düğümlerinin sayfa numaralarının hesaplanmasına olanak tanır.
type: docs
weight: 3320
url: /tr/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Bu sınıf, belge düğümlerinin sayfa numaralarının hesaplanmasına olanak tanır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Sabit Sayfa Formatına Dönüştürme](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokümantasyon makalesi.

```csharp
public class LayoutCollector
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [LayoutCollector](layoutcollector/)(Document) | Bu sınıfın bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Bu toplayıcı örneğinin eklendiği belgeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Toplanan tüm düzen verilerini temizler. Belge manuel olarak güncellendikten veya düzen yeniden oluşturulduktan sonra bu yöntemi çağırın. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(Node) | Düğümün bittiği sayfanın 1 tabanlı dizinini alır. Düğüm bir sayfaya eşlenemiyorsa 0 değerini döndürür. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(Node) | Nesnenin opak konumunu döndürür[`LayoutEnumerator`](../layoutenumerator/) belirtilen düğüme karşılık gelir. Döndürülen değeri argüman olarak kullanabilirsiniz.[`Current`](../layoutenumerator/current/) belgenin numaralandırıldığı ve düğümün belgesinin aynı olduğu göz önüne alındığında. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(Node) | Belirtilen düğümün kapsadığı sayfa sayısını alır. Düğüm tek bir sayfadaysa 0. Bu, şununla aynıdır:[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(Node) | Düğümün başladığı sayfanın 1 tabanlı dizinini alır. Düğüm bir sayfaya eşlenemiyorsa 0 değerini döndürür. |

### Notlar

Bir oluşturduğunuz zaman`LayoutCollector` ve bir belirtin[`Document`](../../aspose.words/document/) Eklenecek belge nesnesi , belge sayfalar halinde formatlandığında, toplayıcı belge düğümlerinin düzen nesnelerine eşlenmesini kaydeder.

Belirli bir belge düğümünün (örneğin çalıştırma, paragraf veya tablo hücresi) hangi sayfada bulunduğunu kullanarak öğrenebilirsiniz.[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) Ve[`GetNumPagesSpanned`](./getnumpagesspanned/)yöntemler. Bu yöntemler, belgenin sayfa düzeni modelini otomatik olarak oluşturur ve gerekirse alanları günceller.

Artık düzen bilgilerini toplamanız gerekmediğinde, en iyisi[`Document`](./document/) mülkiyet`hükümsüz` Daha fazla düzen eşlemesinin gereksiz şekilde toplanmasını önlemek için .

### Örnekler

Bir düğümün kapsadığı sayfa aralıklarının nasıl görüleceğini gösterir.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Belgemizin içeriğinin kaç sayfaya yayıldığını saymak için "GetNumPagesSpanned" yöntemini çağırın.
// Belge boş olduğundan bu sayfa sayısı şu anda sıfırdır.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Belgeyi 5 sayfalık içerikle doldurun.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Düzen toplayıcıdan önce, bize bilgi vermesi için "UpdatePageLayout" yöntemini çağırmamız gerekiyor
// sayfa sayısı gibi düzen ile ilgili herhangi bir ölçüm için doğru bir rakam.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Herhangi bir düğümün başlangıç ve bitiş sayfalarının sayısını ve genel sayfa aralıklarını görebiliriz.
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

// LayoutEnumerator, düzen varlıkları koleksiyonunu bir ağaç gibi geçebilir.
// Bunu herhangi bir düğümün karşılık gelen düzen varlığına da uygulayabiliriz.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)


