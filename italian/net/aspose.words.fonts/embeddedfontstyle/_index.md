---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words per .NET
description: Aspose.Words.Fonts.EmbeddedFontStyle enum. Specifica lo stile di un carattere incorporato allinterno di aFontInfo oggetto in C#.
type: docs
weight: 2860
url: /it/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

Specifica lo stile di un carattere incorporato all'interno di a[`FontInfo`](../fontinfo/) oggetto.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Regular | `0` | Specifica il carattere incorporato regolare. |
| Bold | `1` | Specifica il carattere incorporato Grassetto. |
| Italic | `2` | Specifica il carattere corsivo incorporato. |
| BoldItalic | `3` | Specifica il carattere incorporato grassetto-italico. |

## Esempi

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

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
