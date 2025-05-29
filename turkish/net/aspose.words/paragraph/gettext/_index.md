---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: .NET için Aspose.Words
description: Paragraf sonları dahil olmak üzere metni zahmetsizce almak ve metin işleme verimliliğinizi artırmak için Paragraf GetText yöntemini keşfedin.
type: docs
weight: 280
url: /tr/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

Paragraf sonu karakteri dahil olmak üzere bu paragrafın metnini alır.

```csharp
public override string GetText()
```

## Notlar

Tüm alt düğümlerin metni birleştirilir ve paragraf sonu karakteri aşağıdaki gibi eklenir:

* Eğer paragraf, paragrafın son paragrafıysa[`Body`](../../body/) , sonra [`SectionBreak`](../../controlchar/sectionbreak/) (\x000c) eklendi.
* Eğer paragraf, paragrafın son paragrafıysa[`Cell`](../../../aspose.words.tables/cell/) , sonra [`Cell`](../../controlchar/cell/) (\x0007) eklendi.
* Diğer tüm paragraflar için [`ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) eklendi.

Döndürülen dize, aşağıda açıklandığı gibi tüm denetim ve özel karakterleri içerir[`ControlChar`](../../controlchar/).

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

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
