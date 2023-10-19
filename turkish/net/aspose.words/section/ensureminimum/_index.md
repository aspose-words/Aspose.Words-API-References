---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: Section EnsureMinimum yöntem. Bölümün sahip olmasını sağlarBody biriyleParagraph  C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Bölümün sahip olmasını sağlar[`Body`](../body/) biriyle[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Örnekler

Düzenleme için yeni bir bölüm düğümünün nasıl hazırlanacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge, bir gövdeye sahip olan ve bunun da bir paragrafa sahip olduğu bir bölümle birlikte gelir.
// Bu paragrafa metin dizileri, şekiller veya tablolar gibi öğeler ekleyerek bu belgeye içerik ekleyebiliriz.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Bunun gibi yeni bir bölüm eklersek ne gövdesi ne de başka bir alt düğümü olmayacak.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Düzenlemeye başlamak için bu bölüme bir gövde ve paragraf eklemek üzere "EnsureMinimum" yöntemini çalıştırın.
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
