---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SemiHidden controlla la visibilità degli stili nella galleria Stili e nel riquadro attività, migliorando l'efficienza e il flusso di lavoro di progettazione.
type: docs
weight: 170
url: /it/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

Ottiene/imposta se lo stile viene nascosto dalla galleria Stili e dal riquadro attività Stili.

```csharp
public bool SemiHidden { get; set; }
```

## Esempi

Mostra come dare priorità a uno stile e come nasconderlo.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### Guarda anche

* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
