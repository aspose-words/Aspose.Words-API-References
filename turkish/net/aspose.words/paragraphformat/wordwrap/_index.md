---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words for .NET
description: ParagraphFormat WordWrap mülk. Bu özellik iseYANLIŞ  Bir kelimenin ortasındaki Latince metin geçerli paragraf için kaydırılabilir. Aksi takdirde Latince metin tam kelimelerle sarılır C#'da.
type: docs
weight: 410
url: /tr/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Bu özellik ise`YANLIŞ` , Bir kelimenin ortasındaki Latince metin geçerli paragraf için kaydırılabilir. Aksi takdirde Latince metin tam kelimelerle sarılır.

```csharp
public bool WordWrap { get; set; }
```

## Örnekler

Asya tipografisi için özel özelliklerin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
