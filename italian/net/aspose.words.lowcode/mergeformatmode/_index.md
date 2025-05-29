---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.LowCode.MergeFormatMode per ottimizzare l'unione dei documenti. Migliora il controllo della formattazione quando unisci più file senza sforzo.
type: docs
weight: 4290
url: /it/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

Specifica come viene unita la formattazione quando si combinano più documenti.

```csharp
public enum MergeFormatMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| MergeFormatting | `0` | Combina la formattazione dei documenti uniti. |
| KeepSourceFormatting | `1` | Significa che il documento sorgente manterrà la sua formattazione originale, come stili di carattere, dimensioni, colori, rientri e qualsiasi altro elemento di formattazione applicato al suo contenuto. |
| KeepSourceLayout | `2` | Conserva il layout dei documenti originali nel documento finale. |

## Esempi

Mostra come unire i documenti in un unico documento di output.

```csharp
//Esistono diversi modi per unire i documenti:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
