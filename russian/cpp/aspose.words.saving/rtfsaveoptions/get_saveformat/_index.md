---
title: "Метод Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat. Указывает формат, в котором будет сохранён документ при использовании этого объекта параметров сохранения. Может быть только Rtf в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/rtfsaveoptions/get_saveformat/
---
## RtfSaveOptions::get_SaveFormat method


Указывает формат, в котором будет сохранён документ при использовании этого объекта параметров сохранения. Может быть только [Rtf](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
