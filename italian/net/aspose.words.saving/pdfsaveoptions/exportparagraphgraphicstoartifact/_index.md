---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words per .NET
description: Scopri la proprietà ExportParagraphGraphicsToArtifact di PdfSaveOptions per controllare la grafica dei paragrafi come artefatti, migliorando la chiarezza visiva del tuo documento.
type: docs
weight: 160
url: /it/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Ottiene o imposta un valore che determina se un'immagine di paragrafo deve essere contrassegnata come artefatto.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` e la grafica dei paragrafi (sottolineature, enfasi del testo, ecc.) saranno contrassegnati come "Span" nella struttura logica del documento.

Quando il valore è`VERO` la grafica del paragrafo verrà contrassegnata come "Artefatto".

Questo valore viene ignorato quando[`ExportDocumentStructure`](../exportdocumentstructure/) È`falso` .

## Esempi

Mostra come esportare la grafica dei paragrafi come artefatti (sottolineature, enfasi del testo, ecc.).

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
