---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: FontInfo Name proprietà. Ottiene il nome del carattere in C#.
type: docs
weight: 50
url: /it/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Ottiene il nome del carattere.

```csharp
public string Name { get; }
```

## Osservazioni

Non può essere`nullo`. Può essere una stringa vuota.

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
