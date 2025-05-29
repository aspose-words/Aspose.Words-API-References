---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words per .NET
description: Ottimizza il tuo HTML con la proprietà ExportXhtmlTransitional di HtmlSaveOptions. Controlla le dichiarazioni DOCTYPE per una migliore compatibilità nei formati HTML, MHTML ed EPUB.
type: docs
weight: 280
url: /it/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Specifica se scrivere la dichiarazione DOCTYPE durante il salvataggio in HTML o MHTML. Quando`VERO` , scrive una dichiarazione DOCTYPE nel documento prima dell'elemento radice. Il valore predefinito è`falso`. Quando si salva in EPUB o HTML5 (Html5 ) la dichiarazione DOCTYPE viene sempre scritta.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Osservazioni

Aspose.Words scrive sempre codice HTML ben formato, indipendentemente da questa impostazione.

Quando`VERO`, l'inizio del documento HTML di output apparirà così:

Aspose.Words mira a generare codice XHTML in base alla specifica XHTML 1.0 Transitional, ma l'output non sarà sempre valido rispetto alla DTD. Alcune strutture all'interno di un documento Microsoft Word sono difficili o impossibili da mappare in un documento che sia valido rispetto allo schema XHTML. Ad esempio, XHTML non consente elenchi nidificati (un elemento UL non può essere nidificato all'interno di un altro elemento UL), ma nei documenti Microsoft Word gli elenchi multilivello sono piuttosto frequenti.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//IT"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="it" lang="it">
```

## Esempi

Mostra come visualizzare un'intestazione DOCTYPE durante la conversione di documenti nello standard di transizione Xhtml 1.0.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Il nostro documento conterrà un'intestazione di dichiarazione DOCTYPE solo se abbiamo impostato il flag "ExportXhtmlTransitional" su "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
