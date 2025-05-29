---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà ListExportMode di MarkdownSaveOptions, che controlla come vengono visualizzati gli elementi dell'elenco. Ottimizza i tuoi file con la flessibile MarkdownSyntax!
type: docs
weight: 110
url: /it/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Specifica come gli elementi dell'elenco verranno scritti nel file di output. Il valore predefinito èMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Osservazioni

Quando questa proprietà è impostata suPlainText tutte le etichette degli elenchi vengono aggiornate utilizzando[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) ed esportati con i loro valori effettivi. Tali lists potrebbero non essere compatibili con il formato Markdown e, in questo caso, verranno riconosciuti come testo normale al momento dell'importazione.

Quando questa proprietà è impostata suMarkdownSyntax, l'autore tenta di esportare elementi dell'elenco in un modo che consenta di numerare gli elementi dell'elenco in modalità automatica tramite Markdown.

## Esempi

Mostra come gli elementi dell'elenco verranno scritti nel documento markdown.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Utilizzare MarkdownListExportMode.PlainText o MarkdownListExportMode.MarkdownSyntax per esportare l'elenco.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Guarda anche

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
