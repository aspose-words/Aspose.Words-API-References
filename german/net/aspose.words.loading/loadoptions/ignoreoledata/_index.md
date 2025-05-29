---
title: LoadOptions.IgnoreOleData
linktitle: IgnoreOleData
articleTitle: IgnoreOleData
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die LoadOptions IgnoreOleData-Eigenschaft Ihre Datenverarbeitung verbessert, indem sie Ihnen die Kontrolle über die OLE-Datenverarbeitung ermöglicht. Optimieren Sie noch heute Ihren Workflow!
type: docs
weight: 70
url: /de/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Gibt an, ob die OLE-Daten ignoriert werden sollen.

```csharp
public bool IgnoreOleData { get; set; }
```

## Bemerkungen

Das Ignorieren von OLE-Daten kann den Speicherverbrauch reduzieren und die Leistung steigern, ohne dass Daten verloren gehen, wenn das Zielformat keine OLE-Objekte unterstützt.

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie OLE-Daten beim Laden ignoriert werden.

```csharp
// Das Ignorieren von OLE-Daten kann den Speicherverbrauch reduzieren und die Leistung steigern
// ohne Datenverlust, wenn das Zielformat keine OLE-Objekte unterstützt.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
