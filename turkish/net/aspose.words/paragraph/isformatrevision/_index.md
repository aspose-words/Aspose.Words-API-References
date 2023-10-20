---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words for .NET
description: Paragraph IsFormatRevision mülk. Microsoft Wordde değişiklik izleme etkinken nesnenin biçimlendirmesi değiştirilmişse doğru değerini döndürür C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Microsoft Word'de değişiklik izleme etkinken nesnenin biçimlendirmesi değiştirilmişse doğru değerini döndürür.

```csharp
public bool IsFormatRevision { get; }
```

## Örnekler

Bir paragrafın format revizyonu olup olmadığının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Bu paragraf, mevcut metnin formatını değiştirdiğimizde ortaya çıkan bir "Format" revizyonudur
// "İnceleme" aracılığıyla Microsoft Word'deki revizyonları izlerken -> "Parça değişiklikleri".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
