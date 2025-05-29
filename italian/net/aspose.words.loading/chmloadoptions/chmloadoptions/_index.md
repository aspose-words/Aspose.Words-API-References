---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore ChmLoadOptions per un'inizializzazione fluida. Imposta i valori predefiniti senza sforzo e migliora le prestazioni della tua applicazione oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

Inizializza una nuova istanza di questa classe con valori predefiniti.

```csharp
public ChmLoadOptions()
```

## Esempi

Mostra come risolvere URL come "ms-its:myfile.chm::/index.htm".

```csharp
// Il nostro documento contiene URL come "ms-its:amhelp.chm::....htm", ma ha un nome diverso,
// quindi i collegamenti ai file non funzionano dopo averli salvati in HTML.
// Per evitare questo comportamento, dobbiamo definire il nome del file originale in 'ChmLoadOptions'.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Guarda anche

* class [ChmLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
