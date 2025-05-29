---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.EmbeddedFontFormat, che definisce i formati dei font incorporati nell'oggetto FontInfo per migliorare lo stile dei documenti.
type: docs
weight: 3260
url: /it/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

Specifica il formato di un particolare font incorporato all'interno[`FontInfo`](../fontinfo/) oggetto.

Quando si salva un documento in un file, vengono scritti solo i font incorporati nel formato corrispondente.

```csharp
public enum EmbeddedFontFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| EmbeddedOpenType | `0` | Specifica il formato file Embedded OpenType (EOT). |
| OpenType | `1` | Specifica il font, incorporato come copia semplice del file del font OpenType (TrueType). |

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
