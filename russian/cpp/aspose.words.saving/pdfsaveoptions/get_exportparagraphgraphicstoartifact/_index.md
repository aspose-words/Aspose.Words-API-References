---
title: "метод Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact"
linktitle: "get_ExportParagraphGraphicsToArtifact"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact. Получает или задает значение, определяющее, должна ли графика абзаца быть помечена как артефакт в C++."
type: docs
weight: 17500
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_exportparagraphgraphicstoartifact/
---
## PdfSaveOptions::get_ExportParagraphGraphicsToArtifact method


Получает или задаёт значение, определяющее, следует ли помечать графику абзаца как артефакт.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact() const
```

## Примечания


Значение по умолчанию — **false**, и графика абзаца (подчеркивания, выделение текста и т.д.) будет помечена как "Span" в логической структуре документа.

Когда значение **true**, графика абзаца будет помечена как "Artifact".

Это значение игнорируется, когда [ExportDocumentStructure](../get_exportdocumentstructure/) равно **false**.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
