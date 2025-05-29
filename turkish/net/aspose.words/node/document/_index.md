---
title: Node.Document
linktitle: Document
articleTitle: Document
second_title: .NET için Aspose.Words
description: Node Belge özelliğini keşfedin, sorunsuz veri yönetimi ve gelişmiş üretkenlik için node'unuza bağlı belgeye zahmetsizce erişin.
type: docs
weight: 20
url: /tr/net/aspose.words/node/document/
---
## Node.Document property

Bu düğümün ait olduğu belgeyi alır.

```csharp
public virtual DocumentBase Document { get; }
```

## Notlar

Düğüm, henüz yeni oluşturulmuş olsa bile ve henüz ağaca eklenmemiş olsa bile veya ağaçtan kaldırılmış olsa bile her zaman bir belgeye aittir.

## Örnekler

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

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
