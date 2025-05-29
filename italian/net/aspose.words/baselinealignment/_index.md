---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.BaselineAlignment per un posizionamento preciso dei font. Migliora la formattazione dei tuoi documenti con opzioni di allineamento verticale ottimali.
type: docs
weight: 130
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
| Top | `0` | Si allinea lungo la parte superiore di ogni carattere. |
| Center | `1` | Allinea i punti centrali di ogni font. |
| Baseline | `2` | Si allinea alla linea di base del paragrafo. |
| Bottom | `3` | Si allinea alla parte inferiore di ogni carattere. |
| Auto | `4` | La linea di base viene regolata automaticamente. |

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
