---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words pour .NET
description: XlsxSaveOptions CompressionLevel propriété. Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut estNormal  en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut estNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Exemples

Montre comment compresser un document XLSX.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum; 

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Voir également

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
