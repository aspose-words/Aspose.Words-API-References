---
title: "Метод Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag"
linktitle: "get_ExportFloatingShapesAsInlineTag"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag. Получает или задаёт значение, определяющее, экспортируются ли плавающие объекты как встроенные теги в структуре документа в C++."
type: docs
weight: 16500
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_exportfloatingshapesasinlinetag/
---
## PdfSaveOptions::get_ExportFloatingShapesAsInlineTag method


Получает или задаёт значение, определяющее, экспортировать ли плавающие фигуры как встроенные теги в структуре документа.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag() const
```

## Примечания


Значение по умолчанию — **false**, и плавающие объекты будут экспортированы как блочные теги, размещённые после абзаца, в котором они привязаны.

Когда значение **true**, плавающие объекты будут экспортированы как встроенные теги, размещённые внутри абзаца, в котором они привязаны.

Это значение игнорируется, когда [ExportDocumentStructure](../get_exportdocumentstructure/) равно **false**.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
