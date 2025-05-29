---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words per .NET
description: Scopri il metodo GetFontsSources di FontSettings per accedere facilmente all'array di fonti per i font TrueType in Aspose.Words. Ottimizza la gestione dei tuoi font oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

Ottiene una copia dell'array che contiene l'elenco delle origini in cui Aspose.Words cerca i font TrueType.

```csharp
public FontSourceBase[] GetFontsSources()
```

### Valore di ritorno

Una copia delle sorgenti dei font correnti.

## Osservazioni

Il valore restituito è una copia dei dati utilizzati da Aspose.Words. La modifica di entries nell'array restituito non avrà alcun effetto sul rendering del documento. Per specificare nuove fonti di font, utilizzare[`SetFontsSources`](../setfontssources/) metodo.

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

### Guarda anche

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
