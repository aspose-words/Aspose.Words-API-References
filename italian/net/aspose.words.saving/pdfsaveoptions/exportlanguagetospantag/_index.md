---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words per .NET
description: Scopri la proprietà ExportLanguageToSpanTag di PdfSaveOptions. Controlla l'esportazione del testo in lingua con i tag Span per migliorare la struttura e l'accessibilità del documento.
type: docs
weight: 150
url: /it/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Ottiene o imposta un valore che determina se creare o meno un tag "Span" nella struttura del documento per esportare la lingua del testo.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` l'attributo "Lang" è associato a una sequenza di contenuti contrassegnati in un flusso di contenuti di pagina.

Quando il valore è`VERO` Il tag "Span" viene creato per il testo con language non predefinito e l'attributo "Lang" è associato a questo tag.

Questo valore viene ignorato quando[`ExportDocumentStructure`](../exportdocumentstructure/) È`falso` .

## Esempi

Mostra come creare un tag "Span" nella struttura del documento per esportare la lingua del testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Nota, quando "ExportDocumentStructure" è falso, "ExportLanguageToSpanTag" viene ignorato.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
