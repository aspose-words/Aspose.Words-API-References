---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti con la proprietà ExportGeneratorName di SaveOptions. Incorpora il nome e la versione di Aspose.Words per una migliore tracciabilità. Valore predefinito true.
type: docs
weight: 80
url: /it/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` .

```csharp
public bool ExportGeneratorName { get; set; }
```

## Esempi

Mostra come disabilitare l'aggiunta del nome e della versione di Aspose.Words nei file prodotti.

```csharp
Document doc = new Document();

// Utilizzare https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ per sapere come controllare il risultato.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
