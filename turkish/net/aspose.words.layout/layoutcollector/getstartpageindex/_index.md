---
title: LayoutCollector.GetStartPageIndex
second_title: Aspose.Words for .NET API Referansı
description: LayoutCollector yöntem. Düğümün başladığı sayfanın 1 tabanlı dizinini alır. Düğüm bir sayfaya eşlenemiyorsa 0 değerini döndürür.
type: docs
weight: 70
url: /tr/net/aspose.words.layout/layoutcollector/getstartpageindex/
---
## LayoutCollector.GetStartPageIndex method

Düğümün başladığı sayfanın 1 tabanlı dizinini alır. Düğüm bir sayfaya eşlenemiyorsa 0 değerini döndürür.

```csharp
public int GetStartPageIndex(Node node)
```

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* ad alanı [Aspose.Words.Layout](../../layoutcollector/)
* toplantı [Aspose.Words](../../../)


