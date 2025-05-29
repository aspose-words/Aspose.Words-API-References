---
title: FontInfo.Panose
linktitle: Panose
articleTitle: Panose
second_title: Aspose.Words per .NET
description: Scopri la proprietà PANOSE di FontInfo, ottieni o imposta facilmente il numero di classificazione del carattere per una migliore gestione dei font e una maggiore precisione nel design.
type: docs
weight: 70
url: /it/net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

Ottiene o imposta il numero di classificazione del carattere PANOSE.

```csharp
public byte[] Panose { get; set; }
```

## Osservazioni

PANOSE è una descrizione compatta di 10 byte delle caratteristiche visive critiche di un font, come contrasto, spessore e stile serif. Le cifre rappresentano il tipo di famiglia, lo stile serif, lo spessore, le proporzioni, il contrasto, la variazione del tratto, lo stile del braccio, la forma delle lettere, la linea mediana e l'altezza della X.

Può essere`null`.

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

* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
