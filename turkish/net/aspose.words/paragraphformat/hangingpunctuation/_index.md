---
title: ParagraphFormat.HangingPunctuation
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Geçerli paragraf için asılı noktalamanın etkinleştirilip etkinleştirilmediğini belirten bir bayrak alır veya ayarlar.
type: docs
weight: 120
url: /tr/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Geçerli paragraf için asılı noktalamanın etkinleştirilip etkinleştirilmediğini belirten bir bayrak alır veya ayarlar.

```csharp
public bool HangingPunctuation { get; set; }
```

### Örnekler

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
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


