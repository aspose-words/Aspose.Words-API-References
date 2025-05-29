---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: .NET için Aspose.Words
description: Microsoft Word'deki IsFormatRevision özelliğinin biçimlendirme değişikliklerini nasıl izlediğini, böylece doğru belge düzenlemelerini ve gelişmiş işbirliğini nasıl sağladığını keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Değişiklik izleme etkinleştirilmişken Microsoft Word'de nesnenin biçimlendirmesinin değiştirilmesi durumunda doğru değerini döndürür.

```csharp
public bool IsFormatRevision { get; }
```

## Örnekler

Bir paragrafın biçim revizyonu olup olmadığının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Bu paragraf, mevcut metnin biçimlendirmesini değiştirdiğimizde oluşan bir "Biçim" revizyonudur
// Microsoft Word'de revizyonları "Gözden Geçir" -> "Değişiklikleri İzle" yoluyla izlerken.
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
