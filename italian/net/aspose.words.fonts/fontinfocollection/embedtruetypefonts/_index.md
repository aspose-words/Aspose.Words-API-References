---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words per .NET
description: Scopri come la proprietà EmbedTrueTypeFonts in FontInfoCollection migliora la qualità del documento consentendo l'incorporamento dei font TrueType. Il valore predefinito è false.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Specifica se incorporare o meno i font TrueType in un documento quando viene salvato. Il valore predefinito per questa proprietà è`falso` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Osservazioni

L'incorporamento di font TrueType consente ad altri di visualizzare il documento con gli stessi font utilizzati per crearlo, ma potrebbe aumentare notevolmente le dimensioni del documento.

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
