---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.FontSettings per personalizzare senza sforzo le impostazioni dei font dei documenti, per una migliore leggibilità e una presentazione professionale.
type: docs
weight: 3400
url: /it/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Specifica le impostazioni del font per un documento.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

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
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | Impostazioni predefinite statiche del font. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Impostazioni relative al meccanismo di fallback dei font. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Impostazioni relative al meccanismo di sostituzione dei font. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Ottiene una copia dell'array che contiene l'elenco delle origini in cui Aspose.Words cerca i font TrueType. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Reimposta le sorgenti dei font ai valori predefiniti del sistema. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | Salva la cache di ricerca dei font nel flusso. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | Imposta la cartella in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font. Questa è una scorciatoia per[`SetFontsFolders`](./setfontsfolders/) per impostare una sola directory dei font. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | Imposta le cartelle in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | Imposta le origini in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | Imposta le origini in cui Aspose.Words cerca i font TrueType e carica inoltre la cache di ricerca dei font salvata in precedenza . |

## Osservazioni

Aspose.Words utilizza le impostazioni dei font per risolvere i font nel documento. I font vengono risolti principalmente durante la creazione del layout del documento o il rendering in formati di pagina fissi. Tuttavia, durante il caricamento di alcuni formati, Aspose.Words potrebbe anche richiedere la risoluzione dei font. Ad esempio, quando si caricano documenti HTML, Aspose.Words potrebbe risolvere i font per eseguire il fallback dei font. Pertanto, si consiglia di impostare le impostazioni dei font in [`LoadOptions`](../../aspose.words.loading/loadoptions/) al momento del caricamento del documento. O almeno prima di creare il layout o di renderizzare il documento nel formato a pagina fissa.

Per impostazione predefinita, tutti i documenti utilizzano un'unica istanza di impostazioni di font statico. È possibile accedervi tramite [`DefaultInstance`](./defaultinstance/) proprietà.

La modifica delle impostazioni del font è sicura in qualsiasi momento e da qualsiasi thread. Tuttavia, si consiglia di non modificarle durante l'elaborazione di documenti che utilizzano queste impostazioni. Ciò potrebbe comportare che lo stesso font venga risolto in modo diverso in diverse parti del documento.

## Esempi

Mostra come aggiungere una sorgente font alle nostre sorgenti font esistenti.

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

// Nella sorgente font predefinita mancano due dei font che stiamo utilizzando nel nostro documento.
// Quando salviamo questo documento, Aspose.Words applicherà font di fallback a tutto il testo formattato con font inaccessibili.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Crea una sorgente font da una cartella che contiene font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Applica un nuovo array di sorgenti di font che contiene le sorgenti di font originali, nonché i nostri font personalizzati.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verificare che Aspose.Words abbia accesso a tutti i font richiesti prima di convertire il documento in PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Ripristina le sorgenti dei font originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

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

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
