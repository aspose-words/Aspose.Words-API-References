---
title: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable метод"
linktitle: "get_IsImageAvailable"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable метод. Возвращает true, если текущее изображение доступно для экспорта в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Возвращает **true**, если текущее изображение доступно для экспорта.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Примечания


Некоторые изображения в документе могут быть недоступны, например, если изображение связано и ссылка недоступна или не указывает на действительное изображение. В этом случае Aspose.Words экспортирует значок с красным крестом. Это свойство возвращает **true**, если оригинальное изображение доступно; возвращает **false**, если оригинальное изображение недоступно, и будет предложен значок "no image" для сохранения.

При сохранении групповой формы или формы, не требующей изображения, это свойство всегда **true**.

## См. также

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
