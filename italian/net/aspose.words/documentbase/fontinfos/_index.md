---
title: DocumentBase.FontInfos
second_title: Aspose.Words per .NET API Reference
description: DocumentBase proprietà. Fornisce laccesso alle proprietà dei caratteri utilizzati in questo documento.
type: docs
weight: 30
url: /it/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Fornisce l'accesso alle proprietà dei caratteri utilizzati in questo documento.

```csharp
public FontInfoCollection FontInfos { get; }
```

### Osservazioni

Questa raccolta di definizioni di caratteri viene caricata così com'è dal documento. Le definizioni di caratteri potrebbero essere facoltative, mancanti o incomplete in alcuni documenti.

Non fare affidamento su questa raccolta per accertarti che un particolare carattere sia utilizzato nel documento. Dovresti utilizzare questa raccolta solo per ottenere informazioni sui caratteri che potrebbero essere utilizzati nel documento.

### Esempi

Mostra come stampare i dettagli di quali caratteri sono presenti in un documento.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Stampa tutti i font usati e non utilizzati nel documento.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../documentbase/)
* assemblea [Aspose.Words](../../../)


