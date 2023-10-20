---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words per .NET
description: FontInfoCollection Contains metodo. Determina se la raccolta contiene un carattere con il nome specificato in C#.
type: docs
weight: 60
url: /it/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Determina se la raccolta contiene un carattere con il nome specificato.

```csharp
public bool Contains(string name)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Nome del carattere da individuare senza distinzione tra maiuscole e minuscole. |

### Valore di ritorno

`VERO` se l'oggetto si trova nella collezione; Altrimenti,`falso`.

## Esempi

Mostra informazioni sui caratteri presenti nel documento vuoto.

```csharp
Document doc = new Document();

// Un documento vuoto contiene 3 caratteri predefiniti. Ogni carattere nel documento
// avrà un oggetto FontInfo corrispondente che contiene dettagli su quel carattere.
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
