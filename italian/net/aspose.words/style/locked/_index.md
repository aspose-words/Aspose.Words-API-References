---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words per .NET
description: Scopri la proprietà "Stile bloccato", controlla il blocco degli stili per una maggiore flessibilità di progettazione e coerenza nei tuoi progetti. Scatena la tua creatività oggi stesso!
type: docs
weight: 120
url: /it/net/aspose.words/style/locked/
---
## Style.Locked property

Specifica se questo stile è bloccato.

```csharp
public bool Locked { get; set; }
```

## Esempi

Mostra come bloccare lo stile.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### Guarda anche

* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
