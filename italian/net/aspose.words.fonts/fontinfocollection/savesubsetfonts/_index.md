---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words per .NET
description: Scopri la proprietà SaveSubsetFonts di FontInfoCollection e controlla i sottoinsiemi di font TrueType incorporati nei tuoi documenti per ottimizzare dimensioni e prestazioni dei file.
type: docs
weight: 50
url: /it/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Specifica se salvare o meno un sottoinsieme dei font TrueType incorporati con il documento. Il valore predefinito per questa proprietà è`falso`.

Questa opzione funziona solo quando[`EmbedTrueTypeFonts`](../embedtruetypefonts/) la proprietà è impostata su`VERO`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Osservazioni

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

## Esempi

Mostra come salvare un documento con i font TrueType incorporati.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### Guarda anche

* class [FontInfoCollection](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
