---
title: Node.Document
second_title: Aspose.Words for .NET API Referansı
description: Node mülk. Bu düğümün ait olduğu belgeyi alır.
type: docs
weight: 20
url: /tr/net/aspose.words/node/document/
---
## Node.Document property

Bu düğümün ait olduğu belgeyi alır.

```csharp
public virtual DocumentBase Document { get; }
```

### Notlar

Düğüm, yeni oluşturulmuş ve henüz ağaca eklenmemiş veya ağaçtan kaldırılmış olsa bile, her zaman bir belgeye aittir.

### Örnekler

Bir düğümün nasıl oluşturulacağını ve sahiplik belgesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Bu paragrafı henüz herhangi bir bileşik düğüme alt öğe olarak eklemedik.
Assert.IsNull(para.ParentNode);

// Bir düğüm, başka bir bileşik düğümün uygun bir alt düğüm türüyse,
// yalnızca her iki düğümün de aynı sahip belgesine sahip olması durumunda alt öğe olarak ekleyebiliriz.
// Sahip belgesi, düğümün yapıcısına ilettiğimiz belgedir.
// Bu paragrafı belgeye eklemedik, bu nedenle belge metnini içermiyor.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Belge bu paragrafa sahip olduğu için onun stillerinden birini paragrafın içeriğine uygulayabiliriz.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Bu düğümü belgeye ekleyin ve ardından içeriğini doğrulayın.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* ad alanı [Aspose.Words](../../node/)
* toplantı [Aspose.Words](../../../)


