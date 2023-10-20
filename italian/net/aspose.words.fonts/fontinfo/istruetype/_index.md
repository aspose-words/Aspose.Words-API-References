---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words per .NET
description: FontInfo IsTrueType proprietà. Indica che questo carattere è un carattere TrueType o OpenType anziché un carattere raster o vettoriale. Limpostazione predefinita èVERO  in C#.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Indica che questo carattere è un carattere TrueType o OpenType anziché un carattere raster o vettoriale. L'impostazione predefinita è`VERO` .

```csharp
public bool IsTrueType { get; set; }
```

## Esempi

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

* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
