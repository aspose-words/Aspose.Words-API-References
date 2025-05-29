---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: .NET için Aspose.Words
description: TxtSaveOptions MaxCharactersPerLine'ı keşfedin, daha iyi metin biçimlendirmesi için satır başına karakter sınırlarını kolayca ayarlayın. Sınırsız karakter için varsayılan değer 0'dır.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

Bir satır başına maksimum karakter sayısını belirten bir tamsayı değeri alır veya ayarlar. Varsayılan değer 0'dır, yani sınır yoktur.

```csharp
public int MaxCharactersPerLine { get; set; }
```

## Örnekler

Satır başına maksimum karakter sayısının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Bir satıra izin verilen maksimum karakter sayısını 30 olarak ayarlayın.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### Ayrıca bakınız

* class [TxtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
