---
title: "Метод Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders"
linktitle: "get_ExportImagesForOldReaders"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders. Указывает, записываются ли ключевые слова для \"старых читателей\" в RTF или нет. Это может существенно влиять на размер RTF‑документа. Значение по умолчанию — true в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


Указывает, записываются ли ключевые слова для «старых читателей» в RTF или нет. Это может существенно влиять на размер RTF‑документа. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## Примечания


"Старые читатели" — это приложения до Microsoft Word 97, а также WordPad. Когда эта опция **true**, Aspose.Words записывает дополнительные RTF‑ключевые слова. Эти ключевые слова позволяют документу корректно отображаться при открытии в приложении "старый читатель", но могут значительно увеличить размер документа.

Если установить эту опцию в **false**, то только изображения в форматах WMF, EMF и BMP будут отображаться в "старых читателях".

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
