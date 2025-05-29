---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words per .NET
description: Scopri come l'enum MarkdownListExportMode di Aspose.Words migliora l'esportazione degli elenchi in Markdown, garantendo una formattazione precisa e un'integrazione perfetta per i tuoi documenti.
type: docs
weight: 6040
url: /it/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

Specifica come gli elenchi vengono esportati in Markdown.

```csharp
public enum MarkdownListExportMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| MarkdownSyntax | `0` | Esporta elementi di elenco compatibili con la sintassi Markdown. |
| PlainText | `1` | Esporta gli elementi dell'elenco come testo normale. |

## Esempi

Mostra come gli elementi dell'elenco verranno scritti nel documento markdown.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Utilizzare MarkdownListExportMode.PlainText o MarkdownListExportMode.MarkdownSyntax per esportare l'elenco.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
