---
title: FontInfo.GetEmbeddedFont
second_title: Aspose.Words per .NET API Reference
description: FontInfo metodo. Ottiene un file di font incorporato specifico.
type: docs
weight: 80
url: /it/net/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo.GetEmbeddedFont method

Ottiene un file di font incorporato specifico.

```csharp
public byte[] GetEmbeddedFont(EmbeddedFontFormat format, EmbeddedFontStyle style)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| format | EmbeddedFontFormat | Specifica il formato del carattere da recuperare. |
| style | EmbeddedFontStyle | Specifica lo stile del carattere da recuperare. |

### Valore di ritorno

ritorna`nullo`se il carattere specificato non è incorporato.

### Esempi

Mostra come estrarre un font incorporato da un documento e salvarlo nel file system locale.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// I formati dei caratteri incorporati possono essere diversi in altri formati come .doc.
// Dobbiamo conoscere il formato corretto prima di poter estrarre il carattere.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Inoltre, possiamo convertire il formato OpenType incorporato, che proviene da documenti .doc, in OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Guarda anche

* enum [EmbeddedFontFormat](../../embeddedfontformat/)
* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontinfo/)
* assemblea [Aspose.Words](../../../)


