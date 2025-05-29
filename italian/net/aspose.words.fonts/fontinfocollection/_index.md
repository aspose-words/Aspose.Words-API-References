---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.FontInfoCollection, la soluzione ideale per gestire in modo efficiente i font dei documenti e migliorarne l'aspetto visivo.
type: docs
weight: 3360
url: /it/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Rappresenta una raccolta di font utilizzati in un documento.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Specifica se incorporare o meno i font di sistema nel documento. Il valore predefinito per questa proprietà è`falso`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Specifica se incorporare o meno i font TrueType in un documento quando viene salvato. Il valore predefinito per questa proprietà è`falso` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Ottiene un font con il nome specificato. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Specifica se salvare o meno un sottoinsieme dei font TrueType incorporati con il documento. Il valore predefinito per questa proprietà è`falso`. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Determina se la raccolta contiene un font con il nome specificato. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |

## Osservazioni

Gli articoli sono[`FontInfo`](../fontinfo/) oggetti.

Non creare istanze di questa classe direttamente. Usa il[`FontInfos`](../../aspose.words/documentbase/fontinfos/) proprietà per accedere alla raccolta di font definiti nel documento.

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

* class [FontInfo](../fontinfo/)
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
