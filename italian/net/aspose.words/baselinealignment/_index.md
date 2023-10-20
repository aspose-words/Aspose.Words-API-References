---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words per .NET
description: Aspose.Words.BaselineAlignment enum. Specifica la posizione verticale dei caratteri su una riga in C#.
type: docs
weight: 20
url: /it/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Specifica la posizione verticale dei caratteri su una riga.

```csharp
public enum BaselineAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Top | `0` | Si allinea lungo la parte superiore di ciascun carattere. |
| Center | `1` | Allinea i punti centrali di ciascun carattere. |
| Baseline | `2` | Allinea alla linea di base del paragrafo. |
| Bottom | `3` | Allinea alla parte inferiore di ciascun carattere. |
| Auto | `4` | Il valore di base viene modificato automaticamente. |

## Esempi

Mostra come impostare la posizione verticale dei caratteri su una riga.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
