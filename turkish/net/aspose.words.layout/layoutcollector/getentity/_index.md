---
title: GetEntity
second_title: Aspose.Words for .NET API Referansı
description: LayoutEnumeratoraspose.words.layout/layoutenumerator bu belirtilen düğüme karşılık gelir. Döndürülen değeri bir argüman olarak kullanabilirsiniz.Currentaspose.words.layout/layoutenumerator/current verilen belge numaralandırılmıştır ve düğümün belgesi aynıdır.
type: docs
weight: 50
url: /tr/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

[`LayoutEnumerator`](../../layoutenumerator) bu belirtilen düğüme karşılık gelir. Döndürülen değeri bir argüman olarak kullanabilirsiniz.[`Current`](../../layoutenumerator/current) verilen belge numaralandırılmıştır ve düğümün belgesi aynıdır.

```csharp
public object GetEntity(Node node)
```

### Notlar

Bu yöntem sadece işe yarar[`Paragraph`](../../../aspose.words/paragraph) düğümler ve bölünmez satır içi düğümler, ör.[`BookmarkStart`](../../../aspose.words/bookmarkstart) veya[`Shape`](../../../aspose.words.drawing/shape) için çalışmıyor[`Run`](../../../aspose.words/run) ,[`Cell`](../../../aspose.words.tables/cell)[`Row`](../../../aspose.words.tables/row) veya[`Table`](../../../aspose.words.tables/table) düğümler ve üstbilgi/altbilgi içindeki düğümler.

Varlığın bir için döndürüldüğünü unutmayın.[`Paragraph`](../../../aspose.words/paragraph) düğüm bir paragraf sonu aralığıdır. Üst satıra çıkmak için uygun yöntemi kullanın

Bir[`Run`](../../../aspose.words/run) sonra, it 'den hemen önce yer imi ekleyebilir ve bunun yerine yer imine gidebilirsiniz.

Bir[`Cell`](../../../aspose.words.tables/cell) düğüm sonra bir[`Paragraph`](../../../aspose.words/paragraph) düğümü bu hücrede ve ardından bir üst varlığa yükselir. Aynı yaklaşım aşağıdakiler için de kullanılabilir:[`Row`](../../../aspose.words.tables/row) ve[`Table`](../../../aspose.words.tables/table) düğümler.

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

* class [Node](../../../aspose.words/node)
* class [LayoutCollector](../../layoutcollector)
* ad alanı [Aspose.Words.Layout](../../layoutcollector)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->