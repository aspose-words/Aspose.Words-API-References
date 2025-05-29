---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: .NET için Aspose.Words
description: İçeriğinizi EnsureMinimum yöntemiyle optimize edin; her bölümün daha fazla netlik ve yapı için bir Paragraf içeren bir Gövde içermesini garantileyin.
type: docs
weight: 150
url: /tr/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Bölümün şu şekilde olmasını sağlar:[`Body`](../body/) bir tanesiyle[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Örnekler

Yeni bir bölüm düğümünün düzenlemeye nasıl hazırlanacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge, bir gövdeye sahip bir bölüm ve gövdenin de bir paragrafı ile birlikte gelir.
// Bu paragrafa metin bölümleri, şekiller veya tablolar gibi öğeler ekleyerek belgeye içerik ekleyebiliriz.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Eğer bu şekilde yeni bir bölüm eklersek, bir gövdesi veya başka herhangi bir alt düğümü olmayacaktır.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Bu bölümü düzenlemeye başlamak için "EnsureMinimum" metodunu çalıştırarak bir gövde ve bir paragraf ekleyin.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
