---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: .NET için Aspose.Words
description: ParagraphFormat WordWrap özelliğinin Word'de metin kaydırmayı nasıl etkilediğini keşfedin. Gelişmiş belge okunabilirliği için Latince metin akışını kontrol etmeyi öğrenin.
type: docs
weight: 420
url: /tr/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Bu özellik ise`YANLIŞ` , Bir kelimenin ortasındaki Latin metni, geçerli paragraf için sarılabilir. Aksi takdirde Latin metni tüm kelimeler tarafından sarılır.

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
