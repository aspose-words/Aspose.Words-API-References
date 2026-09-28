---
title: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality метод"
linktitle: "get_JpegQuality"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality метод. Получает или задает значение, определяющее качество JPEG‑изображений внутри PDF‑документа в C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


Получает или задаёт значение, определяющее качество JPEG‑изображений внутри PDF‑документа.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## Примечания


Значение по умолчанию равно 100.

Это свойство используется вместе с параметром [ImageCompression](../get_imagecompression/).

Имеет эффект только когда документ содержит JPEG‑изображения.

Используйте это свойство, чтобы получить или задать качество изображений внутри документа при сохранении в формате PDF. Значение может варьироваться от 0 до 100, где 0 означает наихудшее качество, но максимальное сжатие, а 100 — лучшее качество, но минимальное сжатие. Если качество равно 100 и исходное изображение JPEG, это означает отсутствие сжатия — будут сохранены оригинальные байты.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
