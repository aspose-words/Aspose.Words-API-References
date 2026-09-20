---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts метод"
linktitle: "get_EmbedFullFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts метод. Управляет тем, как шрифты встраиваются в получаемые PDF‑документы в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Контролирует, как шрифты встраиваются в получаемые PDF‑документы.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Примечания


Значение по умолчанию — **false**, что означает, что шрифты подвыбираются перед встраиванием. Подвыбор полезна, если вы хотите уменьшить размер выходного файла. Подвыбор удаляет все неиспользуемые глифы из шрифта.

Когда это значение установлено в **true**, полный файл шрифта встраивается в PDF без подвыборки. Это приведёт к более крупным выходным файлам, но может быть полезным вариантом, если вы хотите позже редактировать полученный PDF (например, добавить больше текста).

Некоторые шрифты большие (несколько мегабайт), и их встраивание без подвыборки приведёт к крупным выходным документам.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
