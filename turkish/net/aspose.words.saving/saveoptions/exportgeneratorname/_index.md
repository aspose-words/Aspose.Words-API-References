---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: .NET için Aspose.Words
description: SaveOptions ExportGeneratorName özelliğiyle belgelerinizi geliştirin. Daha iyi izlenebilirlik için Aspose.Words adını ve sürümünü gömün. Varsayılan, true.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Ne zaman`doğru` , Aspose.Words adının ve sürümünün üretilen dosyalara gömülmesine neden olur. Varsayılan değer`doğru` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## Örnekler

Üretilen dosyalara Aspose.Words adının ve sürümünün eklenmesinin nasıl devre dışı bırakılacağını gösterir.

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
