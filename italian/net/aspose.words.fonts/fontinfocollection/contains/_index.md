---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words per .NET
description: Scopri se FontInfoCollection include un font specifico per nome. Gestisci e accedi facilmente alla tua collezione di font con questo metodo essenziale.
type: docs
weight: 60
url: /it/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Determina se la raccolta contiene un font con il nome specificato.

```csharp
public bool Contains(string name)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Nome del font da individuare, senza distinzione tra maiuscole e minuscole. |

### Valore di ritorno

`VERO`se l'elemento si trova nella raccolta; in caso contrario,`falso`.

## Esempi

Mostra informazioni sui font presenti nel documento vuoto.

```csharp
Document doc = new Document();

// Un documento vuoto contiene 3 font predefiniti. Ogni font nel documento
// avrà un oggetto FontInfo corrispondente che contiene dettagli su quel font.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Guarda anche

* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
