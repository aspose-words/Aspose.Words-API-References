---
title: FontInfoCollection.Item
second_title: Aspose.Words per .NET API Reference
description: FontInfoCollection proprietà. Ottiene un carattere con il nome specificato.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/fontinfocollection/item/
---
## FontInfoCollection indexer (1 of 2)

Ottiene un carattere con il nome specificato.

```csharp
public FontInfo this[string name] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| name | Nome del carattere da individuare senza distinzione tra maiuscole e minuscole. |

### Esempi

Mostra come estrarre un carattere incorporato da un documento e salvarlo nel file system locale.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// I formati dei caratteri incorporati potrebbero essere diversi in altri formati come .doc.
// Dobbiamo conoscere il formato corretto prima di poter estrarre il carattere.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Inoltre, possiamo convertire il formato OpenType incorporato, che proviene da documenti .doc, in OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Guarda anche

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontinfocollection/)
* assemblea [Aspose.Words](../../../)

---

## FontInfoCollection indexer (2 of 2)

Ottiene un carattere all'indice specificato.

```csharp
public FontInfo this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice in base zero del carattere. |

### Esempi

Mostra come estrarre un carattere incorporato da un documento e salvarlo nel file system locale.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// I formati dei caratteri incorporati potrebbero essere diversi in altri formati come .doc.
// Dobbiamo conoscere il formato corretto prima di poter estrarre il carattere.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Inoltre, possiamo convertire il formato OpenType incorporato, che proviene da documenti .doc, in OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Guarda anche

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontinfocollection/)
* assemblea [Aspose.Words](../../../)


