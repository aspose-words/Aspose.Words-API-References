---
title: FontInfo.GetEmbeddedFont
linktitle: GetEmbeddedFont
articleTitle: GetEmbeddedFont
second_title: Aspose.Words per .NET
description: Scopri il metodo FontInfo GetEmbeddedFont per recuperare facilmente specifici file di font incorporati, migliorando i tuoi progetti di design con una tipografia impeccabile.
type: docs
weight: 90
url: /it/net/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo.GetEmbeddedFont method

Ottiene un file di font incorporato specifico.

```csharp
public byte[] GetEmbeddedFont(EmbeddedFontFormat format, EmbeddedFontStyle style)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| format | EmbeddedFontFormat | Specifica il formato del font da recuperare. |
| style | EmbeddedFontStyle | Specifica lo stile del carattere da recuperare. |

### Valore di ritorno

Resi`null` se il font specificato non è incorporato.

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

* enum [EmbeddedFontFormat](../../embeddedfontformat/)
* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
