---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words EmbeddedFontStyle per gestire facilmente gli stili di font incorporati negli oggetti FontInfo, migliorando le capacità di formattazione dei documenti.
type: docs
weight: 3270
url: /it/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Specifica lo stile di un font incorporato all'interno di un[`FontInfo`](../fontinfo/) oggetto.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Regular | `0` | Specifica il font incorporato normale. |
| Bold | `1` | Specifica il font incorporato Bold. |
| Italic | `2` | Specifica il font corsivo incorporato. |
| BoldItalic | `3` | Specifica il font incorporato Grassetto-Corsivo. |

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

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
