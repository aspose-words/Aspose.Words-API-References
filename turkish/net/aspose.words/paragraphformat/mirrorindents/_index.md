---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: .NET için Aspose.Words
description: ParagraphFormat MirrorIndents özelliğinin, tutarlı sol ve sağ girintiler sağlayarak belge biçimlendirmenizi nasıl geliştirdiğini ve cilalı bir görünüm sağladığını keşfedin.
type: docs
weight: 240
url: /tr/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

Sol ve sağ girintilerin aynı genişlikte olup olmadığını belirten bir bayrak alır veya ayarlar.

```csharp
public bool MirrorIndents { get; set; }
```

## Örnekler

Sol ve sağ girintilerin nasıl aynı yapılacağını göster.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
