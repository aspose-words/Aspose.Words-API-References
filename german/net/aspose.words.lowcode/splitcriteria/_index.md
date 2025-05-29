---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.LowCode.SplitCriteria-Aufzählung für effizientes Dokument-Splitting. Optimieren Sie Ihren Workflow mit vielseitigen Optionen für nahtloses Teilemanagement.
type: docs
weight: 4400
url: /de/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

Gibt an, wie das Dokument in Teile aufgeteilt wird.

```csharp
public enum SplitCriteria
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Page | `0` | Gibt an, dass das Dokument in Seiten aufgeteilt ist. |
| SectionBreak | `1` | Gibt an, dass das Dokument bei einem Abschnittsumbruch beliebiger Art in Teile aufgeteilt wird. |
| Style | `2` | Gibt an, dass das Dokument in einem Absatz in Teile aufgeteilt wird, der mit dem in[`SplitStyle`](../splitoptions/splitstyle/) . |

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

* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
