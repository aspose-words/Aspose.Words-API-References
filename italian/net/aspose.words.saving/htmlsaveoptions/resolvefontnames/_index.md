---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words per .NET
description: Scopri come la proprietà HtmlSaveOptions ResolveFontNames migliora la formattazione dei documenti garantendo sostituzioni accurate dei font negli output HTML.
type: docs
weight: 430
url: /it/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Specifica se i nomi delle famiglie di font utilizzati nel documento vengono risolti e sostituiti in base a [`FontSettings`](../../../aspose.words/document/fontsettings/) quando vengono scritti in formati basati su HTML.

```csharp
public bool ResolveFontNames { get; set; }
```

## Osservazioni

Per impostazione predefinita, questa opzione è impostata su`falso` e i nomi delle famiglie di font vengono scritti in HTML come specificato nei documenti sorgente. Vale a dire,[`FontSettings`](../../../aspose.words/document/fontsettings/) vengono ignorati e non viene eseguita alcuna risoluzione o sostituzione dei nomi delle famiglie di font.

Se questa opzione è impostata su`VERO` , Aspose.Words utilizza[`FontSettings`](../../../aspose.words/document/fontsettings/) per risolvere ogni nome di famiglia di font specificato in un documento sorgente nel nome di una famiglia di font disponibile, eseguendo la sostituzione del font secondo necessità.

## Esempi

Mostra come risolvere tutti i nomi dei font prima di scriverli in HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Questo documento contiene testo che nomina un font di cui non disponiamo.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Se non abbiamo modo di ottenere questo font e vogliamo essere in grado di visualizzare tutto il testo
// in questo documento, in un output HTML, possiamo sostituirlo con un altro font.
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
    // Per impostazione predefinita, questa opzione è impostata su "False" e Aspose.Words scrive i nomi dei font come specificato nel documento di origine
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
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
