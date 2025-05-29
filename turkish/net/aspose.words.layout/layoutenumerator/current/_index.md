---
title: LayoutEnumerator.Current
linktitle: Current
articleTitle: Current
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım esnekliği için sayfa düzeni modelinizdeki geçerli konuma kolayca erişmek ve onu değiştirmek üzere LayoutEnumerator Current özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.layout/layoutenumerator/current/
---
## LayoutEnumerator.Current property

Sayfa düzeni modelindeki geçerli konumu alır veya ayarlar. Bu özellik, geçerli düzen varlığına karşılık gelen opak bir nesne döndürür.

```csharp
public object Current { get; set; }
```

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

* class [LayoutEnumerator](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
