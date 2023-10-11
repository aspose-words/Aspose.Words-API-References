---
title: Font.NoProofing
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Biçimlendirilmiş karakterlerin yazım denetimi yapılmaması durumunda doğrudur.
type: docs
weight: 280
url: /tr/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Biçimlendirilmiş karakterlerin yazım denetimi yapılmaması durumunda doğrudur.

```csharp
public bool NoProofing { get; set; }
```

### Örnekler

Metnin Microsoft Word tarafından yazım denetimi yapılmasının nasıl önleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalde Microsoft Word, yazım hatalarını pürüzlü kırmızı bir alt çizgiyle vurgular.
// Metnin bir kısmını oluşturmak için "NoProofing" bayrağının ayarını kaldırabiliriz.
// yazım denetleyiciyi tamamen devre dışı bırakırken atlar.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


