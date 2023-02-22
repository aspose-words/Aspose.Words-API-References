---
title: SaveOptions.ExportGeneratorName
second_title: Aspose.Words for .NET API Referansı
description: SaveOptions mülk. Doğru olduğunda Aspose.Wordsün adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değerdir doğru .
type: docs
weight: 80
url: /tr/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Doğru olduğunda, Aspose.Words'ün adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değerdir **doğru** .

```csharp
public bool ExportGeneratorName { get; set; }
```

### Örnekler

Üretilen dosyalara Aspose.Words adının ve sürümünün eklenmesinin nasıl devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();

// Sonucu nasıl kontrol edeceğinizi öğrenmek için https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ adresini kullanın.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../saveoptions/)
* toplantı [Aspose.Words](../../../)


