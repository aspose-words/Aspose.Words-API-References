---
title: Enum FontFamily
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fonts.FontFamily enum. Rappresenta la famiglia di caratteri.
type: docs
weight: 2910
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
| Auto | `0` | Specifica un nome di famiglia generico. Questo nome viene utilizzato quando le informazioni su un carattere non esistono o non sono importanti. Viene utilizzato il carattere predefinito. |
| Roman | `1` | Specifica un carattere proporzionale con grazie. Un esempio è Times New Roman. |
| Swiss | `2` | Specifica un carattere proporzionale senza grazie. Un esempio è Arial. |
| Modern | `3` | Specifica un carattere a spaziatura fissa con o senza serif. I caratteri a spaziatura fissa sono solitamente moderni; gli esempi includono Pica, Elite e Courier New. |
| Script | `4` | Specifica un carattere progettato per assomigliare alla scrittura a mano; gli esempi includono Script e Corsivo. |
| Decorative | `5` | Specifica un carattere nuovo. Un esempio è l'inglese antico. |

### Osservazioni

Una famiglia di caratteri è un insieme di caratteri con caratteristiche comuni di larghezza del tratto e serif.

### Esempi

Mostra come accedere e stampare i dettagli di ciascun carattere in un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // I nomi alternativi sono generalmente vuoti.
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


