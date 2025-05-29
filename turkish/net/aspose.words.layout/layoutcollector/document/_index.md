---
title: LayoutCollector.Document
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: Gelişmiş iş akışı verimliliği için belge eklerini kolayca yönetmek ve özelleştirmek amacıyla LayoutCollector'ın Belge özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.layout/layoutcollector/document/
---
## LayoutCollector.Document property

Bu toplayıcı örneğinin bağlı olduğu belgeyi alır veya ayarlar.

```csharp
public Document Document { get; set; }
```

## Notlar

Belge düğümlerinin sayfa dizinlerine erişmeniz gerekiyorsa, bu özelliği belgenin sayfa düzeni oluşturulmadan önce bir belge örneğini işaret edecek şekilde ayarlamanız gerekir. Bu özelliği şu şekilde ayarlamak en iyisidir:`hükümsüz` sonrasında, aksi takdirde toplayıcı, belgenin sayfa düzeninin sonraki yeniden yapılandırmalarından bilgi toplamaya devam eder.

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

* class [Document](../../../aspose.words/document/)
* class [LayoutCollector](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
