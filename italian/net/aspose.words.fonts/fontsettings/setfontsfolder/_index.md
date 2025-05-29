---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo SetFontsFolder per specificare una directory di font TrueType in Aspose.Words, migliorando il rendering del documento e l'incorporamento dei font.
type: docs
weight: 80
url: /it/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Imposta la cartella in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font. Questa è una scorciatoia per[`SetFontsFolders`](../setfontsfolders/) per impostare una sola directory dei font.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFolder | String | La cartella che contiene i font TrueType. |
| recursive | Boolean | Vero per eseguire la scansione ricorsiva delle cartelle specificate alla ricerca di font. |

## Esempi

Mostra come impostare una directory sorgente dei font.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Le nostre fonti di font non contengono il font che abbiamo utilizzato per il testo di questo documento.
// Se utilizziamo queste impostazioni del carattere durante il rendering di questo documento,
// Aspose.Words applicherà un font di fallback al testo che contiene un font che Aspose.Words non riesce a trovare.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Nelle sorgenti dei font predefinite mancano i due font che stiamo utilizzando in questo documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Utilizzare il metodo "SetFontsFolder" per impostare una directory che fungerà da nuova sorgente per i font.
// Passare "false" come argomento "ricorsivo" per includere i font da tutti i file di font presenti nella directory
// che stiamo passando nel primo argomento, ma non includiamo alcun font in nessuna delle sottocartelle di quella directory.
// Passare "true" come argomento "ricorsivo" per includere tutti i file di font nella directory che stiamo passando
// nel primo argomento, così come tutti i font nelle sue sottodirectory.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Il font "Amethysta" si trova in una sottocartella della directory dei font.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Ripristina le sorgenti dei font originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Guarda anche

* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
