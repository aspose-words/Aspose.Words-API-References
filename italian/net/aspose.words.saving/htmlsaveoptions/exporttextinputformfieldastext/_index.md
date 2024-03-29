---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportTextInputFormFieldAsText proprietà. Controlla il modo in cui i campi del modulo di input testo vengono salvati in HTML o MHTML. Il valore predefinito èfalso  in C#.
type: docs
weight: 260
url: /it/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Controlla il modo in cui i campi del modulo di input testo vengono salvati in HTML o MHTML. Il valore predefinito è`falso` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Osservazioni

Quando impostato su`VERO` , esporta i campi del modulo di input di testo come testo normale. Quando`falso`, esporta i campi del modulo di input del testo di Word come elementi INPUT in HTML.

Quando si esporta in EPUB, i campi del modulo di immissione testo vengono sempre salvati come testo a causa dei requisiti di questo formato.

## Esempi

Mostra come specificare la cartella per la memorizzazione delle immagini collegate dopo il salvataggio in .html.

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
