---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words per .NET
description: ParagraphFormat BaselineAlignment proprietà. Ottiene o imposta la posizione verticale dei caratteri su una riga in C#.
type: docs
weight: 40
url: /it/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Ottiene o imposta la posizione verticale dei caratteri su una riga.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

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

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
