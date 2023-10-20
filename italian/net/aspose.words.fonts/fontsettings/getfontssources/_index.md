---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words per .NET
description: FontSettings GetFontsSources metodo. Ottiene una copia dellarray che contiene lelenco delle fonti in cui Aspose.Words cerca i caratteri TrueType in C#.
type: docs
weight: 50
url: /it/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

Ottiene una copia dell'array che contiene l'elenco delle fonti in cui Aspose.Words cerca i caratteri TrueType.

```csharp
public FontSourceBase[] GetFontsSources()
```

### Valore di ritorno

Una copia delle origini dei caratteri correnti.

## Osservazioni

Il valore restituito è una copia dei dati utilizzati da Aspose.Words. Se modifichi le voci nell'array restituito, ciò non avrà alcun effetto sul rendering del documento. Per specificare il nuovo font source utilizzare il file[`SetFontsSources`](../setfontssources/) metodo.

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

### Guarda anche

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
