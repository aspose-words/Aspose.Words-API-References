---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: .NET için Aspose.Words
description: Herhangi bir düğümün doğrudan üst düğümüne kolayca erişmek için Node ParentNode özelliğini keşfedin, böylece web geliştirme verimliliğinizi ve kod netliğinizi artırın.
type: docs
weight: 60
url: /tr/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Bu düğümün en yakın üst düğümünü alır.

```csharp
public CompositeNode ParentNode { get; }
```

## Notlar

Bir düğüm yeni oluşturulmuşsa ve henüz ağaca eklenmemişse, veya ağaçtan kaldırılmışsa, üst düğüm`hükümsüz`.

## Örnekler

Bir düğümün üst düğümüne nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Belgenin ilk paragrafına bir alt Çalıştırma düğümü ekle.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// Paragraf, çalıştırma düğümünün ana düğümüdür. Bu soyağacını izleyebiliriz
// belgenin düğüm ağacının kökü olan belge düğümüne kadar.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

Bir düğümün nasıl oluşturulacağını ve ona ait belgenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Bu paragrafı henüz herhangi bir bileşik düğüme alt öğe olarak eklemedik.
Assert.IsNull(para.ParentNode);

// Bir düğüm başka bir bileşik düğümün uygun bir alt düğüm türüyse,
// yalnızca her iki düğümün de aynı sahip belgesi varsa bunu bir çocuk olarak ekleyebiliriz.
// Sahip belgesi, düğümün kurucusuna geçirdiğimiz belgedir.
// Bu paragrafı belgeye eklemediğimiz için belgede metni bulunmuyor.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Belge bu paragrafın sahibi olduğundan, paragrafın içeriğine onun stillerinden birini uygulayabiliriz.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Bu düğümü belgeye ekleyin ve ardından içeriğini doğrulayın.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
