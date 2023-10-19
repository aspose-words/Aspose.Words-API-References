---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words for .NET
description: SaveOptions ExportGeneratorName mülk. Ne zamandoğru  Aspose.Wordsün adının ve sürümünün üretilen dosyalara yerleştirilmesine neden olur. Varsayılan değerdoğru  C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Ne zaman`doğru` , Aspose.Words'ün adının ve sürümünün üretilen dosyalara yerleştirilmesine neden olur. Varsayılan değer:`doğru` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## Örnekler

Aspose.Words'ün adının ve sürümünün üretilen dosyalara eklenmesinin nasıl devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();

// Sonucun nasıl kontrol edileceğini öğrenmek için https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ adresini kullanın.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
