---
title: FontInfo.GetEmbeddedFontAsOpenType
linktitle: GetEmbeddedFontAsOpenType
articleTitle: GetEmbeddedFontAsOpenType
second_title: Aspose.Words per .NET
description: Scopri come il metodo FontInfo GetEmbeddedFontAsOpenType recupera i font incorporati nel formato OpenType, migliorando la flessibilità e la qualità del design.
type: docs
weight: 100
url: /it/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

Ottiene un file di font incorporato in formato OpenType. I font in formato OpenType incorporato vengono convertiti in OpenType.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
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

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
