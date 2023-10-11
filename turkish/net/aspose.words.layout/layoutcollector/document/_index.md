---
title: LayoutCollector.Document
second_title: Aspose.Words for .NET API Referansı
description: LayoutCollector mülk. Bu toplayıcı örneğinin eklendiği belgeyi alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.layout/layoutcollector/document/
---
## LayoutCollector.Document property

Bu toplayıcı örneğinin eklendiği belgeyi alır veya ayarlar.

```csharp
public Document Document { get; set; }
```

### Notlar

Belge düğümlerinin sayfa dizinlerine erişmeniz gerekiyorsa, belgenin sayfa düzeni oluşturulmadan önce bu özelliği bir belge örneğine, işaret edecek şekilde ayarlamanız gerekir. Bu özelliği şu şekilde ayarlamak en iyisidir:`hükümsüz` daha sonra aksi takdirde toplayıcı, belgenin sayfa düzeninin sonraki yeniden oluşturmalarından bilgi toplamaya devam eder.

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

* class [Document](../../../aspose.words/document/)
* class [LayoutCollector](../)
* ad alanı [Aspose.Words.Layout](../../layoutcollector/)
* toplantı [Aspose.Words](../../../)


