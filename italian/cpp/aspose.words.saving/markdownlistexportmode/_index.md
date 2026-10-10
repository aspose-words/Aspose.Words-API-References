---
title: "Enumerazione Aspose::Words::Saving::MarkdownListExportMode"
linktitle: "MarkdownListExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Saving::MarkdownListExportMode. Specifica come le liste vengono esportate in Markdown in C++."
type: docs
weight: 68000
url: /it/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


Specifica come gli elenchi vengono esportati in Markdown.

```cpp
enum class MarkdownListExportMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| MarkdownSyntax | 0 | Esporta gli elementi dell'elenco compatibili con la sintassi Markdown. |
| PlainText | 1 | Esporta gli elementi dell'elenco come testo semplice. |


## Esempi



Mostra come gli elementi dell'elenco verranno scritti nel documento markdown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Usa MarkdownListExportMode.PlainText o MarkdownListExportMode.MarkdownSyntax per esportare l'elenco.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
