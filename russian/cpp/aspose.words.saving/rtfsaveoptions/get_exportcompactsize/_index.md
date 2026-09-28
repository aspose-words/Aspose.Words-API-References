---
title: "Метод Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize"
linktitle: "get_ExportCompactSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize. Позволяет уменьшить размер выходных RTF‑документов, но если они содержат RTL (текст справа налево), он будет отображаться некорректно. Значение по умолчанию — false в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


Позволяет уменьшить размер выходных RTF‑документов, но если они содержат RTL (справа налево) текст, он будет отображаться некорректно. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## Примечания


Если документ, который вы хотите конвертировать в RTF с помощью Aspose.Words, не содержит текста справа налево на таких языках, как арабский, то вы можете установить эту опцию в **true**, чтобы уменьшить размер полученного RTF.

## Примеры



Показывает, как сохранить документ в .rtf с пользовательскими параметрами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Создайте объект \"RtfSaveOptions\", который передадите методу \"Save\" документа, чтобы изменить способ сохранения его в RTF.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// Установите свойство \"ExportCompactSize\" в значение \"true\", чтобы
// уменьшить размер сохранённого документа за счёт совместимости с текстом справа налево.
options->set_ExportCompactSize(true);

// Установите свойство \"ExportImagesFotOldReaders\" в значение \"true\", чтобы использовать дополнительные ключевые слова и гарантировать, что наш документ
// совместим с читателями до Microsoft Word 97 и WordPad.
// Установите свойство \"ExportImagesFotOldReaders\" в значение \"false\", чтобы уменьшить размер документа,
// но при этом предотвратить возможность старым читателям читать любые изображения, не являющиеся метафайлами или BMP, которые могут быть в документе.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## См. также

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
