---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words for .NET
description: LayoutCollector GetEntity yöntem. Nesnenin opak konumunu döndürürLayoutEnumerator belirtilen düğüme karşılık gelir. Döndürülen değeri argüman olarak kullanabilirsiniz.Current belgenin numaralandırıldığı ve düğümün belgesinin aynı olduğu göz önüne alındığında C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Nesnenin opak konumunu döndürür[`LayoutEnumerator`](../../layoutenumerator/) belirtilen düğüme karşılık gelir. Döndürülen değeri argüman olarak kullanabilirsiniz.[`Current`](../../layoutenumerator/current/) belgenin numaralandırıldığı ve düğümün belgesinin aynı olduğu göz önüne alındığında.

```csharp
public object GetEntity(Node node)
```

## Notlar

Bu yöntem yalnızca[`Paragraph`](../../../aspose.words/paragraph/) düğümlerin yanı sıra bölünemez satır içi düğümler, örneğin[`BookmarkStart`](../../../aspose.words/bookmarkstart/) veya[`Shape`](../../../aspose.words.drawing/shape/) . için işe yaramıyor[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) veya[`Table`](../../../aspose.words.tables/table/) düğümler ve üstbilgi/altbilgi içindeki düğümler.

Kuruluşun bir süreliğine geri döndüğünü unutmayın.[`Paragraph`](../../../aspose.words/paragraph/) düğüm bir paragraf sonu aralığıdır. Ana satıra çıkmak için uygun yöntemi kullanın

Bir yere gitmeniz gerekiyorsa[`Run`](../../../aspose.words/run/) metnini seçerseniz it 'den hemen önce yer imini ekleyebilir ve ardından bunun yerine yer imine gidebilirsiniz.

Bir yere gitmeniz gerekiyorsa[`Cell`](../../../aspose.words.tables/cell/) düğüm o zaman bir yere geçebilirsiniz[`Paragraph`](../../../aspose.words/paragraph/)Bu hücredeki düğümünü kullanın ve ardından bir üst varlığa yükselin. Aynı yaklaşım aşağıdakiler için de kullanılabilir:[`Row`](../../../aspose.words.tables/row/) ve[`Table`](../../../aspose.words.tables/table/) düğümler.

## Örnekler

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
