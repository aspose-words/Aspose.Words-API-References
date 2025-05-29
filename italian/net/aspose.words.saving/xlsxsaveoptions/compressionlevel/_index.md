---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words per .NET
description: Scopri la proprietà CompressionLevel di XlsxSaveOptions per ottimizzare il salvataggio dei documenti con impostazioni di compressione personalizzabili per una gestione efficiente dei file.
type: docs
weight: 20
url: /it/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Specifica il livello di compressione utilizzato per salvare il documento. Il valore predefinito èNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Esempi

Mostra come comprimere un documento XLSX.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Guarda anche

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
