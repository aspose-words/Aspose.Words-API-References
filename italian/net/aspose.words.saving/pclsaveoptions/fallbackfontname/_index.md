---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words per .NET
description: PclSaveOptions FallbackFontName proprietà. Nome del carattere che verrà utilizzato se non viene trovato alcun carattere previsto nelle raccolte di caratteri della stampante e incorporati in C#.
type: docs
weight: 20
url: /it/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Nome del carattere che verrà utilizzato se non viene trovato alcun carattere previsto nelle raccolte di caratteri della stampante e incorporati.

```csharp
public string FallbackFontName { get; set; }
```

## Osservazioni

Se non viene trovato alcun fallback, viene generato un avviso e viene utilizzato il carattere "Arial".

## Esempi

Mostra come dichiarare un carattere che una stampante applicherà al testo stampato come sostituto qualora il carattere originale non fosse disponibile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Questo documento istruirà la stampante ad applicare "Times New Roman" al testo con il carattere mancante.
// Se anche "Times New Roman" non fosse disponibile, la stampante utilizzerà per impostazione predefinita il carattere "Arial".
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Guarda anche

* class [PclSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
