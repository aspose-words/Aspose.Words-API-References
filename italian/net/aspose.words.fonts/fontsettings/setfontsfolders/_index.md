---
title: FontSettings.SetFontsFolders
second_title: Aspose.Words per .NET API Reference
description: FontSettings metodo. Imposta le cartelle in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o lincorporamento di caratteri.
type: docs
weight: 90
url: /it/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Imposta le cartelle in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o l'incorporamento di caratteri.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontsFolders | String[] | Un array di cartelle che contengono caratteri TrueType. |
| recursive | Boolean | True per eseguire la scansione ricorsiva delle cartelle specificate alla ricerca di caratteri. |

### Osservazioni

Per impostazione predefinita, Aspose.Words cerca i caratteri installati nel sistema.

L'impostazione di questa proprietà reimposta la cache di tutti i caratteri caricati in precedenza.

### Esempi

Mostra come impostare più directory di origine dei caratteri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Le nostre fonti di carattere non contengono il carattere che abbiamo utilizzato per il testo in questo documento.
// Se utilizziamo queste impostazioni del carattere durante il rendering di questo documento,
// Aspose.Words applicherà un carattere di fallback al testo che ha un carattere che Aspose.Words non riesce a individuare.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Nelle origini dei caratteri predefinite mancano i due caratteri che utilizziamo in questo documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Utilizza il metodo "SetFontsFolders" per creare un'origine dei caratteri da ciascuna directory dei caratteri che passiamo come primo argomento.
// Passa "false" come argomento "ricorsivo" per includere i caratteri da tutti i file di caratteri presenti nelle directory
// che stiamo passando nel primo argomento, ma non includiamo alcun carattere da nessuna delle sottocartelle delle directory.
// Passa "true" come argomento "ricorsivo" per includere tutti i file di caratteri nelle directory che stiamo passando
// nel primo argomento, così come tutti i caratteri nelle relative sottodirectory.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// La cartella "Junction" stessa non contiene file di caratteri, ma ha sottocartelle che li contengono.
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

// Ripristina le origini dei caratteri originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Guarda anche

* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontsettings/)
* assemblea [Aspose.Words](../../../)


