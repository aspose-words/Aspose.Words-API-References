---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die MarkdownListExportMode-Aufzählung von Aspose.Words den Listenexport nach Markdown verbessert und eine präzise Formatierung und nahtlose Integration Ihrer Dokumente gewährleistet.
type: docs
weight: 6040
url: /de/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

Gibt an, wie Listen in Markdown exportiert werden.

```csharp
public enum MarkdownListExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| MarkdownSyntax | `0` | Exportieren Sie Listenelemente, die mit der Markdown-Syntax kompatibel sind. |
| PlainText | `1` | Listenelemente als einfachen Text exportieren. |

## Beispiele

Zeigt, wie Listenelemente in das Markdown-Dokument geschrieben werden.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Verwenden Sie MarkdownListExportMode.PlainText oder MarkdownListExportMode.MarkdownSyntax, um die Liste zu exportieren.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
