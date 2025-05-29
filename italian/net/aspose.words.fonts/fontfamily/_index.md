---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Fonts.FontFamily, la chiave per gestire senza sforzo diverse famiglie di font, migliorando lo stile e la formattazione dei documenti.
type: docs
weight: 3340
url: /it/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

Rappresenta la famiglia di caratteri.

```csharp
public enum FontFamily
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `0` | Specifica un nome di famiglia generico. Questo nome viene utilizzato quando le informazioni su un font non esistono o non sono rilevanti. Viene utilizzato il font predefinito. |
| Roman | `1` | Specifica un font proporzionale con grazie. Un esempio è Times New Roman. |
| Swiss | `2` | Specifica un font proporzionale senza grazie. Un esempio è Arial. |
| Modern | `3` | Specifica un font a spaziatura fissa con o senza grazie. I font a spaziatura fissa sono solitamente moderni; alcuni esempi includono Pica, Elite e Courier New. |
| Script | `4` | Specifica un font progettato per assomigliare alla scrittura a mano; alcuni esempi includono Script e Cursive. |
| Decorative | `5` | Specifica un font originale. Un esempio è l'inglese antico. |

## Osservazioni

Una famiglia di font è un insieme di font che hanno in comune la larghezza del tratto e le caratteristiche serif.

## Esempi

Mostra come accedere e stampare i dettagli di ciascun font in un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // I nomi alt sono solitamente vuoti.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
