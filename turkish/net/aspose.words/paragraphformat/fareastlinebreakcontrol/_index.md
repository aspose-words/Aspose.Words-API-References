---
title: ParagraphFormat.FarEastLineBreakControl
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Geçerli paragrafa Doğu Asya satır kesme kurallarının uygulanıp uygulanmadığını belirten bir bayrak alır veya ayarlar.
type: docs
weight: 100
url: /tr/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Geçerli paragrafa Doğu Asya satır kesme kurallarının uygulanıp uygulanmadığını belirten bir bayrak alır veya ayarlar.

```csharp
public bool FarEastLineBreakControl { get; set; }
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


