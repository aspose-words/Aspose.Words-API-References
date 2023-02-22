---
title: ParagraphFormat.WordWrap
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Bu özellik ise yanlış Bir kelimenin ortasındaki Latince metin geçerli paragraf için sarılabilir. Aksi takdirde Latince metin tam kelimelerle sarılır.
type: docs
weight: 400
url: /tr/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Bu özellik ise **yanlış** Bir kelimenin ortasındaki Latince metin, geçerli paragraf için sarılabilir. Aksi takdirde Latince metin tam kelimelerle sarılır.

```csharp
public bool WordWrap { get; set; }
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


