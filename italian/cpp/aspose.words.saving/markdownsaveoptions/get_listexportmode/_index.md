---
title: "Metodo Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode"
linktitle: "get_ListExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode. Specifica come gli elementi dell'elenco verranno scritti nel file di output. Il valore predefinito è MarkdownSyntax in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


Specifica come gli elementi dell'elenco verranno scritti nel file di output. Il valore predefinito è [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## Note


Quando questa proprietà è impostata su [PlainText](../../markdownlistexportmode/) tutte le etichette dell'elenco vengono aggiornate usando [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) e esportate con i loro valori effettivi. Tali elenchi possono non essere compatibili con il formato Markdown e saranno riconosciuti come testo semplice durante l'importazione in questo caso.

Quando questa proprietà è impostata su [MarkdownSyntax](../../markdownlistexportmode/), lo scrittore tenta di esportare gli elementi dell'elenco in modo da consentire la numerazione automatica degli elementi tramite Markdown.

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

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
