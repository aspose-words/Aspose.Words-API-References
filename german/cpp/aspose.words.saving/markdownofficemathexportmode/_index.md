---
title: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownOfficeMathExportMode‑Enum. Gibt an, wie Aspose.Words OfficeMath in Markdown in C++ exportiert."
type: docs
weight: 68500
url: /de/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


Gibt an, wie Aspose.Words OfficeMath nach Markdown exportiert.

```cpp
enum class MarkdownOfficeMathExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | 0 | Exportiere OfficeMath als Klartext. |
| Image | 1 | Exportiere OfficeMath als Bild. |
| MathML | 2 | Exportiere OfficeMath als MathML. |
| Latex | 3 | Exportiere OfficeMath als LaTeX. |
| MarkItDown | 4 | Exportiere OfficeMath als LaTeX, das mit MarkItDown kompatibel ist. |


## Beispiele



Zeigt, wie OfficeMath in das Dokument geschrieben wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


Zeigt, wie das OfficeMath‑Objekt als LaTeX exportiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


Zeigt, wie das OfficeMath‑Objekt als MarkItDown exportiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
