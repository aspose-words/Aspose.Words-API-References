---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words per .NET
description: FontInfoCollection EmbedTrueTypeFonts proprietà. Specifica se incorporare o meno i caratteri TrueType in un documento quando viene salvato. Il valore predefinito per questa proprietà èfalso  in C#.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Specifica se incorporare o meno i caratteri TrueType in un documento quando viene salvato. Il valore predefinito per questa proprietà è`falso` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Osservazioni

L'incorporamento dei caratteri TrueType consente ad altri di visualizzare il documento con gli stessi caratteri utilizzati per crearlo, ma può aumentare sostanzialmente le dimensioni del documento.

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

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
