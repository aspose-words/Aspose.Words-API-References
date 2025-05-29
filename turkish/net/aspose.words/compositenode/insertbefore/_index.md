---
title: CompositeNode.InsertBefore
linktitle: InsertBefore
articleTitle: InsertBefore
second_title: .NET için Aspose.Words
description: Veri yapınızın yönetimini geliştirerek, referans düğümlerinden önce düğümleri sorunsuz bir şekilde eklemek için CompositeNode InsertBefore yönteminin nasıl kullanılacağını keşfedin.
type: docs
weight: 160
url: /tr/net/aspose.words/compositenode/insertbefore/
---
## CompositeNode.InsertBefore&lt;T&gt; method

Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler.

```csharp
public T InsertBefore<T>(T newChild, Node refChild)
    where T : Node
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newChild | T | The[`Node`](../../node/) eklemek için. |
| refChild | Node | The[`Node`](../../node/) bu referans düğümüdür.*newChild* bu düğümden önce yerleştirilir. |

### Geri dönüş değeri

Eklenen düğüm.

## Notlar

Eğer*refChild* dır`hükümsüz` , ekler*newChild* çocuk düğümlerinin listesinin sonunda.

Eğer*newChild* Ağaçta zaten varsa, önce o kaldırılır.

Eklenen düğüm başka bir belgeden oluşturulduysa, kullanmalısınız[`ImportNode`](../../documentbase/importnode/) Düğümü geçerli belgeye aktarmak için. Daha sonra içe aktarılan düğüm geçerli belgeye eklenebilir.

## Örnekler

CompositeNode'un alt düğüm koleksiyonuna alt düğümlerin nasıl ekleneceğini, güncelleneceğini ve silineceğini gösterir.

```csharp
Document doc = new Document();

// Boş bir belgenin varsayılan olarak bir paragrafı vardır.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Paragrafımızdaki gibi bileşik düğümler, çocuk olarak başka bileşik ve satır içi düğümler içerebilir.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Üç tane daha çalıştırma düğümü oluştur.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Belge gövdesi, bunları bileşik bir düğüme ekleyene kadar bu çalışmaları görüntülemeyecektir
// bu, ilk çalıştırmada yaptığımız gibi, belgenin düğüm ağacının bir parçasıdır.
// Eklediğimiz düğümlerin metin içeriklerinin nereye gideceğini belirleyebiliriz
// paragraftaki başka bir düğüme göre bir ekleme konumu belirtilerek belgede görünür.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// İkinci çalışmayı ilk çalışmanın önündeki paragrafa ekle.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// İlk çalıştırmadan sonra üçüncü çalıştırmayı ekle.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// İlk çalışmayı paragrafın alt düğüm koleksiyonunun başına ekle.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Mevcut alt düğümleri düzenleyerek ve silerek çalıştırmanın içeriğini değiştirebiliriz.
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
