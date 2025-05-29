---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SplitOptions SplitCriteria-Eigenschaft die Dokumentenverwaltung verbessert, indem sie Ihren Inhalt effizient in überschaubare Abschnitte unterteilt.
type: docs
weight: 20
url: /de/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

Gibt die Kriterien für die Aufteilung des Dokuments in Teile an.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## Beispiele

Zeigt, wie ein Dokument nach Seiten aufgeteilt wird.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Siehe auch

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
