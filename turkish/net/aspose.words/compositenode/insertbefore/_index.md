---
title: InsertBefore
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler.
type: docs
weight: 150
url: /tr/net/aspose.words/compositenode/insertbefore/
---
## CompositeNode.InsertBefore method

Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler.

```csharp
public Node InsertBefore(Node newChild, Node refChild)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newChild | Node | Eklenecek Düğüm. |
| refChild | Node | Referans düğüm olan Düğüm. newChild bu düğümden önce yerleştirilir. |

### Geri dönüş değeri

Eklenen düğüm.

### Notlar

refChild null ise, alt düğümler listesinin sonuna newChild ekler.

newChild zaten ağaçtaysa, önce kaldırılır.

Eklenen düğüm başka bir belgeden oluşturulmuşsa, kullanmanız gerekir.[`ImportNode`](../../documentbase/importnode) düğümü geçerli belgeye aktarmak için. Alınan düğüm daha sonra geçerli belgeye eklenebilir.

### Örnekler

Bir CompositeNode'un alt öğeleri koleksiyonunda alt düğümlerin nasıl ekleneceğini, güncelleneceğini ve silineceğini gösterir.

```csharp
Document doc = new Document();

// Varsayılan olarak boş bir belgenin bir paragrafı vardır.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Paragrafımız gibi bileşik düğümler, alt öğe olarak diğer bileşik ve satır içi düğümleri içerebilir.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Üç çalıştırma düğümü daha oluşturun.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Belge gövdesi, biz bunları bir bileşik düğüme ekleyene kadar bu çalıştırmaları görüntülemeyecektir.
// bu, ilk çalıştırmada yaptığımız gibi, belgenin düğüm ağacının bir parçasıdır.
// Eklediğimiz düğümlerin metin içeriklerinin nerede olduğunu belirleyebiliriz
// paragraftaki başka bir düğüme göre bir ekleme konumu belirterek belgede görünür.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// İkinci çalıştırmayı ilk çalıştırmanın önündeki paragrafa ekleyin.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// İlk çalıştırmadan sonra üçüncü çalıştırmayı ekleyin.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// İlk çalıştırmayı paragrafın alt düğüm koleksiyonunun başına ekleyin.
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

* class [Node](../../node)
* class [CompositeNode](../../compositenode)
* ad alanı [Aspose.Words](../../compositenode)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
