---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words per .NET
description: Converti facilmente SaveFormat in LoadFormat con il metodo FileFormatUtil. Semplifica la gestione dei file e migliora la compatibilità oggi stesso!
type: docs
weight: 90
url: /it/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Converte un[`SaveFormat`](../../saveformat/) valore a un[`LoadFormat`](../../loadformat/) valore se possibile.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Genera un errore quando non è possibile convertire. |

## Esempi

Mostra come convertire un formato di salvataggio nel formato di caricamento corrispondente.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Alcuni tipi di file possono contenere documenti salvati ma non caricati tramite Aspose.Words.
// Se proviamo a convertire un formato di salvataggio di questo tipo in un formato di caricamento, verrà generata un'eccezione.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Guarda anche

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
