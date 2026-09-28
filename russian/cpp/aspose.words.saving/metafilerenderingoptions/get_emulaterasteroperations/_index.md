---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations method"
linktitle: "get_EmulateRasterOperations"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations method. Получает или задает значение, определяющее, следует ли эмулировать растровые операции в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Получает или задает значение, определяющее, следует ли эмулировать растровые операции.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Примечания


В метафайлах могут использоваться специфические растровые операции. Их нельзя отобразить напрямую как векторную графику. Эмуляция растровых операций требует частичной растеризации полученной векторной графики, что может повлиять на производительность рендеринга метафайла.

Когда это значение установлено в **true**, Aspose.Words эмулирует растровые операции. Полученный вывод может быть частично растеризован, и производительность может быть ниже.

Когда это значение установлено в **false**, Aspose.Words не эмулирует растровые операции. Когда [Aspose.Words](../../../aspose.words/) сталкивается с растровой операцией в метафайле, он переходит к рендерингу метафайла в bitmap с использованием операционной системы.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию — **true**.
## См. также

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
