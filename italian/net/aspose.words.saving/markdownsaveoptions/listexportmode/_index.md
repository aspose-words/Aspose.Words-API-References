---
title: MarkdownSaveOptions.ListExportMode
second_title: Aspose.Words per .NET API Reference
description: MarkdownSaveOptions proprietà. Specifica come verranno scritti gli elementi dellelenco nel file di output. Il valore predefinito èMarkdownSyntax .
type: docs
weight: 60
url: /it/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Specifica come verranno scritti gli elementi dell'elenco nel file di output. Il valore predefinito èMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

### Osservazioni

Quando questa proprietà è impostata suPlainText tutte le etichette dell'elenco vengono aggiornate utilizzando[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)ed esportati con i loro valori effettivi. Tali elenchi possono non essere compatibili con il formato Markdown e in questo caso verranno riconosciuti come testo normale al momento dell'importazione.

Quando questa proprietà è impostata suMarkdownSyntax, lo scrittore tenta di esportare gli elementi dell'elenco in modo da consentire di numerare gli elementi dell'elenco in modalità automatica tramite Markdown.

### Esempi

Mostra come elencare gli elementi che verranno scritti nel documento di markdown.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Utilizza MarkdownListExportMode.PlainText o MarkdownListExportMode.MarkdownSyntax per esportare l'elenco.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Guarda anche

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../markdownsaveoptions/)
* assemblea [Aspose.Words](../../../)


