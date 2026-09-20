---
title: "Метод Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf. Получает или задает значение, определяющее, как должны отображаться WMF‑метафайлы с вложенными EMF‑метафайлами в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


Получает или задает значение, определяющее, как должны рендериться WMF метафайлы с вложенными EMF метафайлами.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## Примечания


WMF‑метафайлы могут содержать встроенные данные EMF. MS Word в большинстве случаев использует встроенные данные EMF. GDI+ всегда использует данные WMF.

Когда это значение установлено в **true**, Aspose.Words использует встроенные данные EMF при рендеринге.

Когда это значение установлено в **false**, Aspose.Words использует данные WMF при рендеринге.

Эта опция используется только когда метафайл рендерится как векторная графика. При рендеринге метафайла в bitmap данные WMF всегда используются.

Значение по умолчанию — **true**.
## См. также

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
