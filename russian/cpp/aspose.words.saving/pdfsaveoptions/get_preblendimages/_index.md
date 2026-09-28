---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages метод"
linktitle: "get_PreblendImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages метод. Получает или задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным фоном в C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_preblendimages/
---
## PdfSaveOptions::get_PreblendImages method


Получает или задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным фоном.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages() const
```

## Примечания


Предварительное смешивание изображений может улучшить визуальное отображение PDF‑документа в Adobe Reader и устранить артефакты сглаживания.

Чтобы корректно отображать предварительно смешанные изображения, приложение‑просмотрщик PDF должно поддерживать запись /Matte в словаре изображений с мягкой маской. Кроме того, предварительное смешивание изображений может снизить производительность рендеринга PDF.

Значение по умолчанию — **false**.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
