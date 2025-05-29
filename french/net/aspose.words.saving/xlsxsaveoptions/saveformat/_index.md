---
title: XlsxSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SaveFormat de XlsxSaveOptions pour enregistrer sans effort des documents au format Xlsx, garantissant ainsi la compatibilité et la qualité de vos fichiers.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/xlsxsaveoptions/saveformat/
---
## XlsxSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreXlsx .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Exemples

Montre comment compresser un document XLSX.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XlsxSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
