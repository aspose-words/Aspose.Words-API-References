---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die ListExportMode-Eigenschaft von MarkdownSaveOptions, die die Ausgabe von Listenelementen steuert. Optimieren Sie Ihre Dateien mit flexibler MarkdownSyntax!
type: docs
weight: 110
url: /de/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Gibt an, wie Listenelemente in die Ausgabedatei geschrieben werden. Der Standardwert istMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Bemerkungen

Wenn diese Eigenschaft aufPlainText alle Listenbezeichnungen werden aktualisiert mit[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) und mit ihren tatsächlichen Werten exportiert. Solche Listen können nicht mit dem Markdown-Format kompatibel sein und werden in diesem Fall beim Import als einfacher Text erkannt.

Wenn diese Eigenschaft aufMarkdownSyntaxDer Writer versucht, x000d_ Listenelemente so zu exportieren, dass die Listenelemente im automatischen Modus durch Markdown nummeriert werden können.

## Beispiele

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
