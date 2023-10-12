---
title: Class FontInfo
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fonts.FontInfo classe. Specifica le informazioni su un carattere utilizzato nel documento.
type: docs
weight: 2920
url: /it/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Specifica le informazioni su un carattere utilizzato nel documento.

Per saperne di più, visita il[Lavorare con i caratteri](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class FontInfo
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Ottiene o imposta il nome alternativo per il carattere. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Ottiene o imposta il set di caratteri per il carattere. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Ottiene o imposta la famiglia di caratteri a cui appartiene questo carattere. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Indica che questo carattere è un carattere TrueType o OpenType anziché un carattere raster o vettoriale. L'impostazione predefinita è`VERO` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Ottiene il nome del carattere. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Ottiene o imposta il numero di classificazione del carattere tipografico PANOSE. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Il passo indica se il carattere ha passo fisso, spaziatura proporzionale o si basa su un'impostazione predefinita. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(EmbeddedFontFormat, EmbeddedFontStyle) | Ottiene un file di caratteri incorporato specifico. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(EmbeddedFontStyle) | Ottiene un file di caratteri incorporato in formato OpenType. I caratteri nel formato Embedded OpenType vengono convertiti in OpenType. |

### Osservazioni

Non crei direttamente istanze di questa classe. Usa il[`FontInfos`](../../aspose.words/documentbase/fontinfos/) proprietà per accedere alla raccolta di caratteri definiti in un documento.

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

### Guarda anche

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)


