---
title: "Aspose::Words::Saving::MarkdownLinkExportMode enum"
linktitle: "MarkdownLinkExportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownLinkExportMode Enum. Gibt an, wie Links in Markdown in C++ exportiert werden."
type: docs
weight: 67000
url: /de/cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


Gibt an, wie Links in Markdown exportiert werden.

```cpp
enum class MarkdownLinkExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | 0 | Exportmodus für jeden Link automatisch erkennen. |
| Inline | 1 | Alle Links als Inline-Blöcke exportieren. |
| Referenz | 2 | Alle Links als Referenzblöcke exportieren. |


## Beispiele



Zeigt, wie Links in die .md-Datei geschrieben werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// Bild wird als Referenz geschrieben:
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Bild wird als Inline geschrieben:
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
