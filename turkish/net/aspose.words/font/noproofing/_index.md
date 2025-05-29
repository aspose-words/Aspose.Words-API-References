---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: .NET için Aspose.Words
description: Font NoProofing'i keşfedin. Daha temiz tasarımlar için biçimlendirilmiş metinlerde yazım denetimini önleyin. Belgelerinizi hassasiyet ve profesyonellikle geliştirin!
type: docs
weight: 280
url: /tr/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Biçimlendirilmiş karakterlerin yazım denetimi yapılmayacaksa doğrudur.

```csharp
public bool NoProofing { get; set; }
```

## Örnekler

Microsoft Word tarafından metnin yazım denetiminin nasıl önleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalde Microsoft Word, yazım hatalarını keskin kırmızı bir alt çizgiyle vurgular.
// Metnin bir kısmını oluşturmak için "NoProofing" bayrağını kaldırabiliriz.
// yazım denetimini tamamen devre dışı bırakarak onu atlatır.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
