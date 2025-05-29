---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words per .NET
description: Scopri come gestire le impostazioni di Priorità Stile per ottimizzare l'ordinamento degli stili nel riquadro attività. Migliora il tuo flusso di lavoro con un'organizzazione efficiente degli stili!
type: docs
weight: 160
url: /it/net/aspose.words/style/priority/
---
## Style.Priority property

Ottiene/imposta il valore intero che rappresenta la priorità per l'ordinamento degli stili nel riquadro attività Stili.

```csharp
public int Priority { get; set; }
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
