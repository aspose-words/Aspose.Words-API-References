---
title: FontInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontInfoCollection Item per recuperare facilmente i font in base al nome, migliorando i tuoi progetti di design con precisione e stile.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/fontinfocollection/item/
---
## FontInfoCollection indexer (1 of 2)

Ottiene un font con il nome specificato.

```csharp
public FontInfo this[string name] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| name | Nome del font da individuare, senza distinzione tra maiuscole e minuscole. |

## Esempi

Mostra come estrarre un font incorporato da un documento e salvarlo nel file system locale.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// I formati dei font incorporati potrebbero essere diversi in altri formati, ad esempio .doc.
// Dobbiamo conoscere il formato corretto prima di poter estrarre il font.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Inoltre, possiamo convertire il formato OpenType incorporato, proveniente dai documenti .doc, in OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Guarda anche

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## FontInfoCollection indexer (2 of 2)

Ottiene un font all'indice specificato.

```csharp
public FontInfo this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice del font basato su zero. |

## Esempi

Mostra come estrarre un font incorporato da un documento e salvarlo nel file system locale.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// I formati dei font incorporati potrebbero essere diversi in altri formati, ad esempio .doc.
// Dobbiamo conoscere il formato corretto prima di poter estrarre il font.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Inoltre, possiamo convertire il formato OpenType incorporato, proveniente dai documenti .doc, in OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Guarda anche

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
