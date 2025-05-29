---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SplitOptions SplitCriteria migliora la gestione dei documenti suddividendo in modo efficiente il contenuto in sezioni gestibili.
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

Specifica i criteri per suddividere il documento in parti.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## Esempi

Mostra come dividere un documento in base alle pagine.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Guarda anche

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
