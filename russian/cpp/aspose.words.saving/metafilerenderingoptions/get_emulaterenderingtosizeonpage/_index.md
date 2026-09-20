---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method. Получает или задает значение, определяющее, будет ли рендеринг метафайла эмулировать отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию в C++."
type: docs
weight: 4334
url: /ru/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


Получает или задает значение, определяющее, будет ли рендеринг метафайла эмулировать отображение метафайла в соответствии с размером на странице или отображение метафайла в его размере по умолчанию.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## Примечания


Когда метафайлы отображаются в MS Word, некоторые графические элементы могут масштабироваться в соответствии с фактическим размером метафайла в пикселях. То есть даже масштабирование может влиять на отображение метафайла.

Когда это значение установлено в **true**, Aspose.Words эмулирует рендеринг в соответствии с размером метафайла на странице. Размер в пикселях рассчитывается из размера метафайла на странице и указанного параметра [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/).

Когда это значение установлено в **false**, Aspose.Words эмулирует рендеринг метафайла в его размер по умолчанию в пикселях.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию — **true**.
## См. также

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
