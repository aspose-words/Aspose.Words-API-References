---
title: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode метод"
linktitle: "get_FontEmbeddingMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode метод. Указывает режим встраивания шрифтов в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


Указывает режим встраивания шрифтов.

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## Примечания


Значение по умолчанию — [EmbedAll](../../pdffontembeddingmode/).

Этот параметр работает только с текстом в кодировке ANSI (Windows-1252). Если документ содержит не ANSI текст, соответствующие шрифты будут внедрены независимо от этого параметра.

Соответствие PDF/A и PDF/UA требует внедрения всех шрифтов. Значение [EmbedAll](../../pdffontembeddingmode/) будет использоваться автоматически при сохранении в PDF/A и PDF/UA.
## См. также

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
