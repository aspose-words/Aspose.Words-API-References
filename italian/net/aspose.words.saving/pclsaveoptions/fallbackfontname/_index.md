---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FallbackFontName di PclSaveOptions, che garantisce una stampa senza interruzioni con un font predefinito quando il font desiderato non è disponibile.
type: docs
weight: 20
url: /it/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Nome del font che verrà utilizzato se non viene trovato alcun font previsto nelle raccolte di font della stampante e dei font incorporati.

```csharp
public string FallbackFontName { get; set; }
```

## Osservazioni

Se non viene trovato alcun fallback, viene generato un avviso e viene utilizzato il font "Arial".

## Esempi

Mostra come dichiarare un font che una stampante applicherà al testo stampato come sostituto nel caso in cui il font originale non sia disponibile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Questo documento indicherà alla stampante di applicare il carattere "Times New Roman" al testo con il font mancante.
// Se anche il font "Times New Roman" non fosse disponibile, la stampante utilizzerà per impostazione predefinita il font "Arial".
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Guarda anche

* class [PclSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
