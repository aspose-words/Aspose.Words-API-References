---
title: PdfSaveOptions.ExportLanguageToSpanTag
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Ottiene o imposta un valore che determina se creare o meno un tag Span nella struttura del documento per esportare la lingua del testo.
type: docs
weight: 130
url: /it/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Ottiene o imposta un valore che determina se creare o meno un tag "Span" nella struttura del documento per esportare la lingua del testo.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

### Osservazioni

Il valore predefinito è`falso` e l'attributo "Lang" è allegato a una sequenza di contenuto contrassegnato in un flusso di contenuto di una pagina.

Quando il valore è`VERO` Il tag "Span" viene creato per il testo con language non predefinito e l'attributo "Lang" è allegato a questo tag.

Questo valore viene ignorato quando[`ExportDocumentStructure`](../exportdocumentstructure/) è`falso` .

### Esempi

Mostra come creare un tag "Span" nella struttura del documento per esportare la lingua del testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Nota, quando "ExportDocumentStructure" è false, "ExportLanguageToSpanTag" viene ignorato.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


