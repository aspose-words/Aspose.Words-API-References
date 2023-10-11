---
title: Node.ParentNode
second_title: Aspose.Words for .NET API Referansı
description: Node mülk. Bu düğümün doğrudan ebeveynini alır.
type: docs
weight: 60
url: /tr/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Bu düğümün doğrudan ebeveynini alır.

```csharp
public CompositeNode ParentNode { get; }
```

### Notlar

Bir düğüm yeni oluşturulmuş ve ağaca henüz eklenmemişse, veya ağaçtan kaldırılmışsa ebeveyn düğümdür.`hükümsüz`.

### Örnekler

Bir düğümün üst düğümüne nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Belgenin ilk paragrafına bir alt Çalıştır düğümü ekleyin.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// Paragraf, çalıştırma düğümünün üst düğümüdür. Bu soyun izini sürebiliriz
// belgenin düğüm ağacının kökü olan belge düğümüne kadar.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

Bir düğümün nasıl oluşturulacağını ve sahiplik belgesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Bu paragrafı henüz alt öğe olarak herhangi bir bileşik düğüme eklemedik.
Assert.IsNull(para.ParentNode);

// Bir düğüm başka bir bileşik düğümün uygun bir alt düğüm tipi ise,
// ancak her iki düğümün de aynı sahip belgesine sahip olması durumunda onu çocuk olarak ekleyebiliriz.
// Sahip belgesi, düğümün yapıcısına ilettiğimiz belgedir.
// Bu paragrafı belgeye eklemedik, dolayısıyla belge metnini içermiyor.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Belge bu paragrafın sahibi olduğundan, onun stillerinden birini paragrafın içeriğine uygulayabiliriz.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Bu düğümü belgeye ekleyin ve ardından içeriğini doğrulayın.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* ad alanı [Aspose.Words](../../node/)
* toplantı [Aspose.Words](../../../)


