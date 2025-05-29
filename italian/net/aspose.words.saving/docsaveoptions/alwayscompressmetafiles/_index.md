---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words per .NET
description: Ottimizza la gestione dei documenti con la proprietà AlwaysCompressMetafiles. Migliora le prestazioni controllando la compressione dei metafile per una maggiore efficienza.
type: docs
weight: 20
url: /it/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

Quando`falso` , i metafile di piccole dimensioni non vengono compressi per motivi di prestazioni. Il valore predefinito è`VERO` , tutti i metafile vengono compressi indipendentemente dalla loro dimensione.

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## Esempi

Mostra come modificare la compressione dei metafile in un documento durante il salvataggio.

```csharp
// Aprire un documento contenente una formula di Microsoft Equation 3.0.
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// Quando salviamo un documento, i metafile più piccoli non vengono compressi per motivi di prestazioni.
// Possiamo impostare un flag in un oggetto SaveOptions per comprimere ogni metafile durante il salvataggio.
// Alcuni editor come LibreOffice non riescono a leggere metafile non compressi.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### Guarda anche

* class [DocSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
