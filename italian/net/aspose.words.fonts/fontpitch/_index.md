---
title: FontPitch Enum
linktitle: FontPitch
articleTitle: FontPitch
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Fonts.FontPitch, un potente strumento per gestire gli stili dei font e migliorare la formattazione dei documenti nelle tue applicazioni.
type: docs
weight: 3390
url: /it/net/aspose.words.fonts/fontpitch/
---
## FontPitch enumeration

Rappresenta il passo del carattere.

```csharp
public enum FontPitch
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Specifica che non sono disponibili informazioni sul passo di un font. |
| Fixed | `1` | Specifica che questo è un font a larghezza fissa. |
| Variable | `2` | Specifica che questo è un font a larghezza proporzionale. |

## Osservazioni

Il passo indica se il font è a passo fisso, proporzionalmente spaziato o si basa su un'impostazione predefinita.

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
