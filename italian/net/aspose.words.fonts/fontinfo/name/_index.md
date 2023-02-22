---
title: FontInfo.Name
second_title: Aspose.Words per .NET API Reference
description: FontInfo proprietà. Ottiene il nome del font.
type: docs
weight: 50
url: /it/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Ottiene il nome del font.

```csharp
public string Name { get; }
```

### Osservazioni

Non può essere`nullo`. Può essere una stringa vuota.

### Esempi

Mostra come stampare i dettagli di quali font sono presenti in un documento.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Stampa tutti i caratteri usati e non utilizzati nel documento.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Guarda anche

* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontinfo/)
* assemblea [Aspose.Words](../../../)


