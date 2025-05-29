---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words per .NET
description: Accedi alle proprietà dettagliate dei font con la funzionalità FontInfos di DocumentBase, migliorando senza sforzo il design e la leggibilità del tuo documento.
type: docs
weight: 30
url: /it/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Fornisce l'accesso alle proprietà dei font utilizzati in questo documento.

```csharp
public FontInfoCollection FontInfos { get; }
```

## Osservazioni

Questa raccolta di definizioni di font viene caricata così com'è dal documento. In alcuni documenti le definizioni di font potrebbero essere facoltative, mancanti o incomplete.

Non fare affidamento su questa raccolta per accertare che nel documento sia utilizzato un particolare font. Dovresti usare questa raccolta solo per ottenere informazioni sui font che potrebbero essere utilizzati nel documento.

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

Mostra come stampare i dettagli dei font presenti in un documento.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Stampa tutti i font utilizzati e non utilizzati nel documento.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Guarda anche

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
