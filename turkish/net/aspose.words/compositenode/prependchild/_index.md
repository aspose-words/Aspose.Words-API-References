---
title: CompositeNode.PrependChild
linktitle: PrependChild
articleTitle: PrependChild
second_title: Aspose.Words for .NET
description: CompositeNode PrependChild yöntem. Belirtilen düğümü bu düğüm için alt düğümler listesinin başına ekler C#'da.
type: docs
weight: 150
url: /tr/net/aspose.words/compositenode/prependchild/
---
## CompositeNode.PrependChild method

Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler.

```csharp
public Node PrependChild(Node newChild)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newChild | Node | Eklenecek düğüm. |

### Geri dönüş değeri

Düğüm eklendi.

## Notlar

Eğer*newChild* zaten ağaçtaysa, önce kaldırılır.

Eklenen düğüm başka bir belgeden oluşturulmuşsa kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. İçe aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

## Örnekler

CompositeNode'un alt öğeleri koleksiyonuna alt düğümlerin nasıl ekleneceğini, güncelleştirileceğini ve silineceğini gösterir.

```csharp
Document doc = new Document();

// Boş bir belgede varsayılan olarak bir paragraf bulunur.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Paragrafımız gibi kompozit düğümler çocuk olarak diğer kompozit ve satır içi düğümleri de içerebilir.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Üç tane daha çalıştırma düğümü oluşturun.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Belge gövdesi, biz bunları bir bileşik düğüme ekleyene kadar bu işlemleri görüntülemeyecektir
// ilk çalıştırmada yaptığımız gibi bu da belgenin düğüm ağacının bir parçası.
// Eklediğimiz düğümlerin metin içeriklerinin nerede olduğunu belirleyebiliriz
// paragraftaki başka bir düğüme göre ekleme konumunu belirterek belgede görünür.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// İkinci çalıştırmayı paragrafın ilk çalıştırmanın önüne ekleyin.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// İlk çalıştırmadan sonra üçüncü çalıştırmayı ekleyin.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// İlk çalıştırmayı paragrafın alt düğüm koleksiyonunun başlangıcına ekleyin.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Mevcut alt düğümleri düzenleyip silerek çalıştırmanın içeriğini değiştirebiliriz.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
