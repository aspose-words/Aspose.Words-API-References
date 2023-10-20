---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words per .NET
description: FontInfoCollection SaveSubsetFonts proprietà. Specifica se salvare o meno un sottoinsieme dei caratteri TrueType incorporati con il documento. Il valore predefinito per questa proprietà èfalso in C#.
type: docs
weight: 50
url: /it/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Specifica se salvare o meno un sottoinsieme dei caratteri TrueType incorporati con il documento. Il valore predefinito per questa proprietà è`falso`.

Questa opzione funziona solo quando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) la proprietà è impostata su`VERO`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Osservazioni

Questa opzione funziona solo con i formati DOC, DOCX e RTF.

## Esempi

Mostra come salvare un documento con caratteri TrueType incorporati.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Guarda anche

* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
