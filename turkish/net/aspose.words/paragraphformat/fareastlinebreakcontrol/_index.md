---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words for .NET
description: ParagraphFormat FarEastLineBreakControl mülk. Geçerli paragrafa Doğu Asya satır sonu kurallarının uygulanıp uygulanmadığını belirten bir bayrak alır veya ayarlar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Geçerli paragrafa Doğu Asya satır sonu kurallarının uygulanıp uygulanmadığını belirten bir bayrak alır veya ayarlar.

```csharp
public bool FarEastLineBreakControl { get; set; }
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
