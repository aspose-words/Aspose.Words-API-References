---
title: MarkdownSaveOptions.ListExportMode
second_title: Aspose.Words für .NET-API-Referenz
description: MarkdownSaveOptions eigendom. Gibt an wie Listenelemente in die Ausgabedatei geschrieben werden. Der Standardwert istMarkdownSyntax .
type: docs
weight: 60
url: /de/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Gibt an, wie Listenelemente in die Ausgabedatei geschrieben werden. Der Standardwert istMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

### Bemerkungen

Wenn diese Eigenschaft auf festgelegt istPlainText Alle Listenbezeichnungen werden mit aktualisiert[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)und mit ihren tatsächlichen Werten exportiert. Solche Listen sind möglicherweise nicht mit dem Markdown-Format kompatibel und werden in diesem Fall beim Import als einfacher Text erkannt.

Wenn diese Eigenschaft auf festgelegt istMarkdownSyntax, versucht der Autor, Listenelemente auf eine Weise zu exportieren, die es ermöglicht, Listenelemente im automatischen Modus durch Markdown zu nummerieren.

### Beispiele

Zeigt, wie Listenelemente in das Markdown-Dokument geschrieben werden.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Verwenden Sie MarkdownListExportMode.PlainText oder MarkdownListExportMode.MarkdownSyntax, um die Liste zu exportieren.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Siehe auch

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../markdownsaveoptions/)
* Montage [Aspose.Words](../../../)


