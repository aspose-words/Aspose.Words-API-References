---
title: LayoutCollector
second_title: Aspose.Words for .NET API Referansı
description: Bu sınıf belge düğümlerinin sayfa numaralarını hesaplamaya izin verir.
type: docs
weight: 3120
url: /tr/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Bu sınıf, belge düğümlerinin sayfa numaralarını hesaplamaya izin verir.

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
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Toplanan tüm yerleşim verilerini temizler. Belge manuel olarak güncellendikten veya düzen yeniden oluşturulduktan sonra bu yöntemi çağırın. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(Node) | Düğümün bittiği sayfanın 1 tabanlı dizinini alır. Düğüm bir sayfaya eşlenemiyorsa 0 döndürür. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(Node) | [`LayoutEnumerator`](../layoutenumerator/) bu belirtilen düğüme karşılık gelir. Döndürülen değeri bir argüman olarak kullanabilirsiniz.[`Current`](../layoutenumerator/current/) verilen belge numaralandırılmıştır ve düğümün belgesi aynıdır. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(Node) | Belirtilen düğümün kapsadığı sayfa sayısını alır. 0 düğüm tek bir sayfa içindeyse. Bu aynı[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(Node) | Düğümün başladığı sayfanın 1 tabanlı dizinini alır. Düğüm bir sayfaya eşlenemiyorsa 0 döndürür. |

### Notlar

oluşturduğunuzda[`LayoutCollector`](./layoutcollector/) ve bir belirtin[`Document`](../../aspose.words/document/)eklenecek belge nesnesi, toplayıcı, belge sayfalara biçimlendirildiğinde belge düğümlerinin yerleşim nesnelerine eşlenmesini kaydeder.

Belirli bir belge düğümünün (örneğin, çalışma, paragraf veya tablo hücresi) hangi sayfada olduğunu kullanarak bulabileceksiniz.[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) ve[`GetNumPagesSpanned`](./getnumpagesspanned/) yöntemler. Bu yöntemler, belgenin sayfa yerleşim modelini otomatik olarak oluşturur ve gerekirse alanları günceller.

Artık düzen bilgisi toplamanız gerekmediğinde, en iyisi[`Document`](./document/) daha fazla düzen eşlemelerinin gereksiz şekilde toplanmasını önlemek için özelliği null olarak ayarlayın.

### Örnekler

Bir düğümün yaydığı sayfa aralıklarının nasıl görüneceğini gösterir.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Belgemizin içeriğinin kaç sayfaya yayıldığını saymak için "GetNumPagesSpanned" yöntemini çağırın.
// Belge boş olduğundan, o sayfa sayısı şu anda sıfırdır.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Belgeyi 5 sayfa içerikle doldurun.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// layout toplayıcıdan önce bize verecek "UpdatePageLayout" yöntemini çağırmamız gerekiyor.
// sayfa sayısı gibi mizanpajla ilgili herhangi bir ölçüm için doğru bir rakam.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Herhangi bir düğümün başlangıç ve bitiş sayfalarının numaralarını ve bunların genel sayfa aralıklarını görebiliriz.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Bir LayoutEnumerator kullanarak düzen varlıklarını yineleyebiliriz.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator, bir ağaç gibi düzen varlıklarının koleksiyonunu geçebilir.
// Herhangi bir düğümün karşılık gelen düzen varlığına da uygulayabiliriz.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
