---
title: PclSaveOptions.SaveFormat
second_title: Aspose.Words per .NET API Reference
description: PclSaveOptions proprietà. Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto opzioni di salvataggio. Può esserePcl .
type: docs
weight: 40
url: /it/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto opzioni di salvataggio. Può esserePcl .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Esempi

Mostra come rasterizzare elementi complessi durante il salvataggio di un documento su PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PclSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pclsaveoptions/)
* assemblea [Aspose.Words](../../../)


