---
title: HtmlSaveOptions.ResolveFontNames
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica se i nomi delle famiglie di caratteri utilizzati nel documento vengono risolti e sostituiti in base a FontSettings quando viene scritto in formati basati su HTML.
type: docs
weight: 410
url: /it/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Specifica se i nomi delle famiglie di caratteri utilizzati nel documento vengono risolti e sostituiti in base a [`FontSettings`](../../../aspose.words/document/fontsettings/) quando viene scritto in formati basati su HTML.

```csharp
public bool ResolveFontNames { get; set; }
```

### Osservazioni

Per impostazione predefinita, questa opzione è impostata su`falso` e i nomi delle famiglie di caratteri vengono scritti in HTML come specificato nei documenti di origine. Questo è,[`FontSettings`](../../../aspose.words/document/fontsettings/) vengono ignorati e non viene eseguita alcuna risoluzione o sostituzione dei nomi delle famiglie di caratteri.

Se questa opzione è impostata su`VERO` , Aspose.Words utilizza[`FontSettings`](../../../aspose.words/document/fontsettings/) per risolvere ogni nome di famiglia di caratteri specificato in un documento di origine nel nome di una famiglia di caratteri disponibile, eseguendo la sostituzione di caratteri come richiesto.

### Esempi

Mostra come risolvere tutti i nomi dei caratteri prima di scriverli in HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Questo documento contiene testo che nomina un carattere che non abbiamo.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Se non abbiamo modo di ottenere questo carattere e vogliamo essere in grado di visualizzare tutto il testo
// in questo documento in un output HTML, possiamo sostituirlo con un altro carattere.
FontSettings fontSettings = new FontSettings
{
    SubstitutionSettings =
    {
        DefaultFontSubstitution =
        {
            DefaultFontName = "Arial",
            Enabled = true
        }
    }
};

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // Per impostazione predefinita, questa opzione è impostata su 'False' e Aspose.Words scrive i nomi dei caratteri come specificato nel documento sorgente
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.True(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


