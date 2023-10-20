---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: Paragraph GetText yöntem. Paragraf sonu karakteri de dahil olmak üzere bu paragrafın metnini alır C#'da.
type: docs
weight: 260
url: /tr/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

Paragraf sonu karakteri de dahil olmak üzere bu paragrafın metnini alır.

```csharp
public override string GetText()
```

## Notlar

Tüm alt düğümlerin metni birleştirilir ve paragraf sonu karakteri aşağıdaki gibi eklenir:

* Paragraf son paragraf ise[`Body`](../../body/) , ardından [`SectionBreak`](../../controlchar/sectionbreak/) (\x000c) eklenir.
* Paragraf son paragraf ise[`Cell`](../../../aspose.words.tables/cell/) , ardından [`Cell`](../../controlchar/cell/) (\x0007) eklenir.
* Diğer tüm paragraflar için [`ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) eklenir.

Döndürülen dize, yukarıda açıklandığı gibi tüm kontrol ve özel karakterleri içerir.[`ControlChar`](../../controlchar/).

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

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
