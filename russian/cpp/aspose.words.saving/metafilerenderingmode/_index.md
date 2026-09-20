---
title: "Aspose::Words::Saving::MetafileRenderingMode enum"
linktitle: "MetafileRenderingMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MetafileRenderingMode enum. Указывает, как Aspose.Words должен рендерить метафайлы WMF и EMF в C++."
type: docs
weight: 69000
url: /ru/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


Указывает, как Aspose.Words должен отображать метафайлы WMF и EMF.

```cpp
enum class MetafileRenderingMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words пытается отрисовать метафайл как векторную графику. Если Aspose.Words не может корректно отрисовать некоторые записи метафайла в векторную графику, то Aspose.Words отрисовывает этот метафайл в виде растрового изображения. |
| Vector | 1 | Aspose.Words отображает метафайл как векторную графику. |
| Bitmap | 2 | Aspose.Words вызывает GDI+ для рендеринга метафайла в bitmap, а затем сохраняет bitmap в выходной документ. |

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
