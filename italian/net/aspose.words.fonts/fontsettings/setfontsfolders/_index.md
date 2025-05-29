---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo SetFontsFolders in Aspose.Words per personalizzare le posizioni dei font TrueType per un rendering e un incorporamento ottimali dei documenti.
type: docs
weight: 90
url: /it/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Imposta le cartelle in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontsFolders | String[] | Una serie di cartelle contenenti i font TrueType. |
| recursive | Boolean | Vero per eseguire la scansione ricorsiva delle cartelle specificate alla ricerca di font. |

## Osservazioni

Per impostazione predefinita, Aspose.Words cerca i font installati nel sistema.

Impostando questa proprietà si reimposta la cache di tutti i font caricati in precedenza.

## Esempi

Mostra come impostare più directory di origine dei font.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Le nostre fonti di font non contengono il font che abbiamo utilizzato per il testo di questo documento.
// Se utilizziamo queste impostazioni del carattere durante il rendering di questo documento,
// Aspose.Words applicherà un font di fallback al testo che contiene un font che Aspose.Words non riesce a trovare.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Nelle sorgenti dei font predefinite mancano i due font che stiamo utilizzando in questo documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Utilizzare il metodo "SetFontsFolders" per creare una sorgente font da ogni directory font che passiamo come primo argomento.
// Passare "false" come argomento "ricorsivo" per includere i font da tutti i file di font presenti nelle directory
// che stiamo passando nel primo argomento, ma non includiamo alcun font da nessuna delle sottocartelle delle directory.
// Passare "true" come argomento "ricorsivo" per includere tutti i file di font nelle directory che stiamo passando
// nel primo argomento, così come tutti i font nelle loro sottodirectory.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// La cartella "Junction" non contiene file di font, ma ha delle sottocartelle che li contengono.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Ripristina le sorgenti dei font originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Guarda anche

* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
