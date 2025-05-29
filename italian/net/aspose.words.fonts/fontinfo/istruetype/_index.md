---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsTrueType di FontInfo, che garantisce che il tuo font sia TrueType o OpenType per una qualità superiore, perfetto per design nitidi e scalabili.
type: docs
weight: 50
url: /it/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Indica che questo font è un font TrueType o OpenType anziché un font raster o vettoriale. Il valore predefinito è`VERO` .

```csharp
public bool IsTrueType { get; set; }
```

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

* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
