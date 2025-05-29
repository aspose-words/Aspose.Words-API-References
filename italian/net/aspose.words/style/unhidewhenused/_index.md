---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words per .NET
description: Scopri come gestire la proprietà UnhideWhenUsed per gli stili. Controlla la visibilità nella galleria Stili e nel riquadro attività per migliorare il design del tuo documento.
type: docs
weight: 210
url: /it/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

Ottiene/imposta se lo stile utilizzato nel documento corrente viene visualizzato nella galleria Stili e nel riquadro attività Stili. Vero quando lo stile utilizzato deve essere visualizzato nella galleria Stili.

```csharp
public bool UnhideWhenUsed { get; set; }
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
