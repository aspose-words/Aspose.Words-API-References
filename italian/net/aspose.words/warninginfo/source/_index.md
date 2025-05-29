---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words per .NET
description: Scopri la proprietà WarningInfo Source che rivela l'origine degli avvisi, migliorando l'affidabilità della tua applicazione e l'esperienza utente.
type: docs
weight: 20
url: /it/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Restituisce la fonte dell'avviso.

```csharp
public WarningSource Source { get; }
```

## Esempi

Mostra come lavorare con la sorgente di avviso.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Guarda anche

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
