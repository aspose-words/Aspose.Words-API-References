---
title: "Aspose::Words::Saving::MarkdownListExportMode enum"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownListExportMode enum. Gibt an, wie Listen in Markdown in C++ exportiert werden."
type: docs
weight: 68000
url: /de/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


Gibt an, wie Listen in Markdown exportiert werden.

```cpp
enum class MarkdownListExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| MarkdownSyntax | 0 | Exportiert Listenelemente, die mit der Markdown‑Syntax kompatibel sind. |
| PlainText | 1 | Exportiere Listenelemente als Klartext. |


## Beispiele



Zeigt, wie Listenelemente in das Markdown-Dokument geschrieben werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Verwenden Sie MarkdownListExportMode.PlainText oder MarkdownListExportMode.MarkdownSyntax, um die Liste zu exportieren.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
