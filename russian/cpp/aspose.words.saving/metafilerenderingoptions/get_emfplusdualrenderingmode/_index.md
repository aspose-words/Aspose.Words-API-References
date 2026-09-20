---
title: "Метод Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode. Получает или задает значение, определяющее, как должны отображаться метафайлы EMF+ Dual в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


Получает или задает значение, определяющее, как должны рендериться метафайлы EMF+ Dual.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## Примечания


Метафайлы EMF+ Dual содержат как части EMF+, так и EMF. MS Word и GDI+ всегда отображают часть EMF+. В настоящее время Aspose.Words не полностью поддерживает все записи EMF+, и в некоторых случаях результат рендеринга части EMF выглядит лучше, чем результат рендеринга части EMF+.

Эта опция используется только когда метафайл рендерится как векторная графика. При рендеринге метафайла в bitmap часть EMF+ всегда используется.

Значение по умолчанию — [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## См. также

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
