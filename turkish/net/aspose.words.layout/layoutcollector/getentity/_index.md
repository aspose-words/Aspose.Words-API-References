---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: .NET için Aspose.Words
description: LayoutCollector GetEntity metodunu keşfedin, sorunsuz belge gezintisi ve gelişmiş üretkenlik için LayoutEnumerator'ın konumunu zahmetsizce alın.
type: docs
weight: 50
url: /tr/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Opak bir konumu döndürür[`LayoutEnumerator`](../../layoutenumerator/) belirtilen düğüme karşılık gelen. Döndürülen değeri bir argüman olarak kullanabilirsiniz[`Current`](../../layoutenumerator/current/) verilen belge numaralandırılmıştır ve düğümün belgesi aynıdır.

```csharp
public object GetEntity(Node node)
```

## Notlar

Bu yöntem yalnızca şu amaçlar için işe yarar:[`Paragraph`](../../../aspose.words/paragraph/) düğümler, bölünemez satır içi düğümler gibi, örneğin[`BookmarkStart`](../../../aspose.words/bookmarkstart/) veya[`Shape`](../../../aspose.words.drawing/shape/) . için işe yaramıyor[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) veya[`Table`](../../../aspose.words.tables/table/) düğümler ve başlık/altbilgi içindeki düğümler.

Bir varlık için döndürülen varlığın[`Paragraph`](../../../aspose.words/paragraph/)düğüm bir paragraf sonu aralığıdır. Üst satıra çıkmak için uygun yöntemi kullanın

Eğer bir yere gitmeniz gerekiyorsa[`Run`](../../../aspose.words/run/) metnin hemen öncesine yer imi ekleyebilir ve ardından yer imine gidebilirsiniz.

Eğer bir yere gitmeniz gerekiyorsa[`Cell`](../../../aspose.words.tables/cell/) düğümden sonra başka bir düğüme geçebilirsiniz[`Paragraph`](../../../aspose.words/paragraph/) Bu hücrede düğümü ve ardından bir üst varlığa yükselin. Aynı yaklaşım şu şekilde de kullanılabilir:[`Row`](../../../aspose.words.tables/row/) ve[`Table`](../../../aspose.words.tables/table/) düğümler.

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
