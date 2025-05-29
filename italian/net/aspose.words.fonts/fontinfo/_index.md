---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.FontInfo, la chiave per ottenere informazioni dettagliate sui font dei documenti, migliorando la qualità del testo e l'attrattiva visiva.
type: docs
weight: 3350
url: /it/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Specifica informazioni su un font utilizzato nel documento.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class FontInfo
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Ottiene o imposta il nome alternativo per il font. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Ottiene o imposta il set di caratteri per il font. |
| [EmbeddingLicensingRights](../../aspose.words.fonts/fontinfo/embeddinglicensingrights/) { get; } | Ottiene i diritti di licenza del font incorporato. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Ottiene o imposta la famiglia di font a cui appartiene questo font. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Indica che questo font è un font TrueType o OpenType anziché un font raster o vettoriale. Il valore predefinito è`VERO` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Ottiene il nome del font. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Ottiene o imposta il numero di classificazione del carattere PANOSE. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Il passo indica se il font è a passo fisso, spaziato proporzionalmente o si basa su un'impostazione predefinita. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | Ottiene un file di font incorporato specifico. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | Ottiene un file di font incorporato in formato OpenType. I font in formato OpenType incorporato vengono convertiti in OpenType. |

## Osservazioni

Non creare istanze di questa classe direttamente. Utilizzare il[`FontInfos`](../../aspose.words/documentbase/fontinfos/) proprietà per accedere alla raccolta di fonts definiti in un documento.

## Esempi

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

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
