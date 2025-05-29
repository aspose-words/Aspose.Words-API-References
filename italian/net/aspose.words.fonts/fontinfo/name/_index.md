---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri la proprietà Nome FontInfo per accedere facilmente ai nomi dei font e utilizzarli per una tipografia migliorata nei tuoi progetti.
type: docs
weight: 60
url: /it/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Ottiene il nome del font.

```csharp
public string Name { get; }
```

## Osservazioni

Non può essere`null`Può essere una stringa vuota.

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
