---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.LowCode.SplitCriteria per una suddivisione efficiente dei documenti. Ottimizza il tuo flusso di lavoro con opzioni versatili per una gestione fluida delle parti.
type: docs
weight: 4400
url: /it/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

Specifica come il documento è suddiviso in parti.

```csharp
public enum SplitCriteria
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Page | `0` | Specifica che il documento è suddiviso in pagine. |
| SectionBreak | `1` | Specifica che il documento viene diviso in parti in caso di interruzione di sezione di qualsiasi tipo. |
| Style | `2` | Specifica che il documento è diviso in parti in un paragrafo formattato utilizzando lo stile specificato in[`SplitStyle`](../splitoptions/splitstyle/) . |

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

* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
