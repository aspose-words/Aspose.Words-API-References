---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts метод"
linktitle: "get_UseCoreFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts метод. Получает или задает значение, определяющее, заменять ли TrueType‑шрифты Arial, Times New Roman, Courier New и Symbol на базовые шрифты PDF Type 1 в C++."
type: docs
weight: 32000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


Получает или задает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol на базовые шрифты PDF Type 1.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Примечания


Значение по умолчанию — **false**. Когда это значение установлено в **true**, шрифты Arial, Times New Roman, Courier New и Symbol заменяются в PDF‑документе соответствующими базовыми шрифтами Type 1.

Базовые шрифты PDF, их метрики и подходящие заменяющие шрифты должны быть доступны любому приложению‑просмотрщику PDF.

Этот параметр работает только с текстом в кодировке ANSI (Windows‑1252). Текст вне ANSI будет записываться с внедрённым TrueType‑шрифтом независимо от этой настройки.

Соответствие PDF/A и PDF/UA требует встраивания всех шрифтов. Значение **false** будет использоваться автоматически при сохранении в PDF/A и PDF/UA.

Базовые шрифты не поддерживаются при сохранении в формат PDF 2.0. Значение **false** будет использоваться автоматически при сохранении в PDF 2.0.

Этот параметр имеет более высокий приоритет, чем параметр [FontEmbeddingMode](../get_fontembeddingmode/).
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
