---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportTextInputFormFieldAsText di HtmlSaveOptions ottimizza i campi dei moduli di immissione testo per un salvataggio HTML o MHTML senza interruzioni. Migliora il tuo processo di esportazione!
type: docs
weight: 260
url: /it/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Controlla come i campi del modulo di input di testo vengono salvati in HTML o MHTML. Il valore predefinito è`falso` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Osservazioni

Quando impostato su`VERO` , esporta i campi del modulo di immissione testo come testo normale. Quando`falso`, esporta i campi del modulo di immissione testo di Word come elementi INPUT in HTML.

Durante l'esportazione in EPUB, i campi del modulo di immissione testo vengono sempre salvati come testo due per rispettare i requisiti di questo formato.

## Esempi

Mostra come specificare la cartella in cui archiviare le immagini collegate dopo averle salvate in formato .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Imposta un'opzione per esportare i campi del modulo come testo normale anziché come elementi di input HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
