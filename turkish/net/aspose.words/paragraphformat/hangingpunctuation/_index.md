---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: .NET için Aspose.Words
description: ParagraphFormat'taki Asılı Noktalama özelliğiyle metin düzeninizi nasıl geliştireceğinizi keşfedin. Okunabilirliği ve stili zahmetsizce optimize edin!
type: docs
weight: 130
url: /tr/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Mevcut paragraf için asılı noktalama işaretinin etkinleştirilip etkinleştirilmediğini belirten bir bayrak alır veya ayarlar.

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
