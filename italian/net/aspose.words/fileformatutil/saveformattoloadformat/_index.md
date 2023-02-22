---
title: FileFormatUtil.SaveFormatToLoadFormat
second_title: Aspose.Words per .NET API Reference
description: FileFormatUtil metodo. Converte aSaveFormat valore ad aLoadFormat valore se possibile.
type: docs
weight: 90
url: /it/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Converte a[`SaveFormat`](../../saveformat/) valore ad a[`LoadFormat`](../../loadformat/) valore se possibile.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Lancia quando non può convertire. |

### Esempi

Mostra come convertire un formato di salvataggio nel formato di caricamento corrispondente.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Alcuni tipi di file possono avere documenti salvati ma non caricati usando Aspose.Words.
// Se proviamo a convertire un formato di salvataggio di questo tipo in un formato di caricamento, verrà generata un'eccezione.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Guarda anche

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../fileformatutil/)
* assemblea [Aspose.Words](../../../)


