---
title: "Aspose::Words::Saving::MarkdownListExportMode enum"
linktitle: "MarkdownListExportMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownListExportMode enum. Anger hur listor exporteras till Markdown i C++."
type: docs
weight: 68000
url: /sv/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


Anger hur listor exporteras till Markdown.

```cpp
enum class MarkdownListExportMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| MarkdownSyntax | 0 | Exportera listobjekt som är kompatibla med Markdown-syntax. |
| PlainText | 1 | Exportera listobjekt som vanlig text. |


## Exempel



Visar hur listobjekt kommer att skrivas till markdown-dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Använd MarkdownListExportMode.PlainText eller MarkdownListExportMode.MarkdownSyntax för att exportera listan.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
