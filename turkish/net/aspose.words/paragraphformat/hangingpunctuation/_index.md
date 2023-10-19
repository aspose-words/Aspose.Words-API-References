---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words for .NET
description: ParagraphFormat HangingPunctuation mülk. Geçerli paragraf için asılı noktalama işaretlerinin etkinleştirilip etkinleştirilmediğini gösteren bir bayrak alır veya ayarlar C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Geçerli paragraf için asılı noktalama işaretlerinin etkinleştirilip etkinleştirilmediğini gösteren bir bayrak alır veya ayarlar.

```csharp
public bool HangingPunctuation { get; set; }
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
