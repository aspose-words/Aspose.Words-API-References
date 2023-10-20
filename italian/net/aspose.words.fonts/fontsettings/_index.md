---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words per .NET
description: Aspose.Words.Fonts.FontSettings classe. Specifica le impostazioni del carattere per un documento in C#.
type: docs
weight: 2970
url: /it/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Specifica le impostazioni del carattere per un documento.

Per saperne di più, visita il[Lavorare con i caratteri](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class FontSettings
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FontSettings](fontsettings/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | Impostazioni carattere predefinite statiche. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Impostazioni relative al meccanismo di fallback dei caratteri. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Impostazioni relative al meccanismo di sostituzione dei caratteri. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Ottiene una copia dell'array che contiene l'elenco delle fonti in cui Aspose.Words cerca i caratteri TrueType. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Reimposta le origini dei caratteri sui valori predefiniti del sistema. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | Salva la cache di ricerca dei caratteri nello stream. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | Imposta la cartella in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o l'incorporamento di caratteri. Questa è una scorciatoia per[`SetFontsFolders`](./setfontsfolders/) per impostare una sola directory di caratteri. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | Imposta le cartelle in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o l'incorporamento di caratteri. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | Imposta le origini in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o l'incorporamento di caratteri. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | Imposta le origini in cui Aspose.Words cerca i caratteri TrueType e inoltre carica la cache di ricerca dei caratteri precedentemente salvata . |

## Osservazioni

Aspose.Words utilizza le impostazioni dei caratteri per risolvere i caratteri nel documento. I caratteri vengono risolti principalmente durante la creazione di layout del documento o il rendering in formati di pagina fissi. Ma quando si caricano alcuni formati, Aspose.Words potrebbe anche richiedere la risoluzione dei caratteri. Ad esempio, quando carica documenti HTML Aspose.Words può risolvere i caratteri per eseguire il fallback dei caratteri. Pertanto si consiglia di configurare le impostazioni del carattere in [`LoadOptions`](../../aspose.words.loading/loadoptions/) durante il caricamento del documento. O almeno prima di creare il layout o di rendere il documento nel formato a pagina fissa.

Per impostazione predefinita, tutti i documenti utilizzano un'unica istanza di impostazioni dei caratteri statici. È possibile accedervi da [`DefaultInstance`](./defaultinstance/) proprietà.

La modifica delle impostazioni dei caratteri è sicura in qualsiasi momento da qualsiasi thread. Ma si consiglia di non modificare le impostazioni del carattere durante l'elaborazione di alcuni documenti che utilizzano queste impostazioni. Ciò può portare al fatto che lo stesso carattere verrà risolto diversamente in diverse parti del documento.

## Esempi

Mostra come aggiungere una fonte di carattere alle nostre fonti di carattere esistenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Nella fonte di carattere predefinita mancano due dei caratteri che stiamo utilizzando nel nostro documento.
// Quando salviamo questo documento, Aspose.Words applicherà i caratteri di fallback a tutto il testo formattato con caratteri inaccessibili.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Crea un'origine dei caratteri da una cartella che contiene i caratteri.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Applica una nuova serie di fonti di caratteri che contiene le fonti di caratteri originali, nonché i nostri caratteri personalizzati.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verifica che Aspose.Words abbia accesso a tutti i caratteri richiesti prima di eseguire il rendering del documento in PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Ripristina le origini dei caratteri originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Mostra come impostare una directory di origine dei caratteri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Le nostre fonti di carattere non contengono il carattere che abbiamo utilizzato per il testo in questo documento.
// Se utilizziamo queste impostazioni del carattere durante il rendering di questo documento,
// Aspose.Words applicherà un carattere di fallback al testo che ha un carattere che Aspose.Words non riesce a individuare.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Nelle origini dei caratteri predefinite mancano i due caratteri che utilizziamo in questo documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Utilizza il metodo "SetFontsFolder" per impostare una directory che fungerà da nuova origine dei caratteri.
// Passa "false" come argomento "ricorsivo" per includere i caratteri da tutti i file di caratteri presenti nella directory
// che stiamo passando nel primo argomento, ma non includiamo alcun carattere in nessuna delle sottocartelle di quella directory.
// Passa "true" come argomento "ricorsivo" per includere tutti i file di caratteri nella directory che stiamo passando
// nel primo argomento, così come tutti i caratteri nelle sue sottodirectory.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Il carattere "Amethysta" si trova in una sottocartella della directory dei caratteri.
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

// Ripristina le origini dei caratteri originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

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

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
