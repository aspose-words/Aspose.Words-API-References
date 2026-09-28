---
title: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics метод"
linktitle: "get_CacheBackgroundGraphics"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics метод. Получает или задает значение, определяющее, следует ли кэшировать графику, размещённую в фоне документа, в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_cachebackgroundgraphics/
---
## PdfSaveOptions::get_CacheBackgroundGraphics method


Получает или задаёт значение, определяющее, кэшировать ли графику, размещённую в фоне документа.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics() const
```

## Примечания


Значение по умолчанию — **true**, и графика фона записывается в PDF‑документ как xObject.

Когда значение **false**, графика фона не кэшируется.

Некоторые фигуры не поддерживаются для кэширования (фигуры с полями, закладками, HRefs).

[Document](../../../aspose.words/document/) background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page. 
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
