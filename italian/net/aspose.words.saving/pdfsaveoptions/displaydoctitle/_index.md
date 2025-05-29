---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words per .NET
description: Scopri come la proprietà DisplayDocTitle di PdfSaveOptions migliora la tua esperienza PDF mostrando i titoli dei documenti nella barra del titolo di Windows per una facile identificazione.
type: docs
weight: 90
url: /it/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Flag che specifica se la barra del titolo della finestra deve visualizzare il titolo del documento tratto dalla voce Titolo del dizionario delle informazioni sul documento.

```csharp
public bool DisplayDocTitle { get; set; }
```

## Osservazioni

Se`falso`, la barra del titolo dovrebbe invece visualizzare il nome del file PDF contenente il documento.

Questo flag è richiesto per la conformità PDF/UA.`VERO` il valore verrà utilizzato automaticamente durante il salvataggio di in PDF/UA.

Il valore predefinito è`falso`.

## Esempi

Mostra come visualizzare il titolo del documento come barra del titolo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
// Imposta "DisplayDocTitle" su "true" per ottenere alcuni lettori PDF, come Adobe Acrobat Pro,
// per visualizzare il valore della proprietà incorporata "Titolo" del documento nella scheda che appartiene a questo documento.
// Impostare "DisplayDocTitle" su "false" per far sì che tali lettori visualizzino il nome file del documento.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
