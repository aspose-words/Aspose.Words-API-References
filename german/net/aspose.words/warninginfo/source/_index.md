---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „WarningInfo Source“, die den Ursprung von Warnungen offenlegt und so die Zuverlässigkeit und Benutzerfreundlichkeit Ihrer Anwendung verbessert.
type: docs
weight: 20
url: /de/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Gibt die Quelle der Warnung zurück.

```csharp
public WarningSource Source { get; }
```

## Beispiele

Zeigt, wie mit der Warnquelle gearbeitet wird.

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

### Siehe auch

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
