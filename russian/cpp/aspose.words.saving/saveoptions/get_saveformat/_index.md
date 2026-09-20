---
title: "Метод Aspose::Words::Saving::SaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::SaveOptions::get_SaveFormat. Указывает формат, в котором будет сохраняться документ, если этот объект параметров сохранения используется в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.saving/saveoptions/get_saveformat/
---
## SaveOptions::get_SaveFormat method


Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения.

```cpp
virtual Aspose::Words::SaveFormat Aspose::Words::Saving::SaveOptions::get_SaveFormat()=0
```


## Примеры



Показывает, как использовать определённую кодировку при сохранении документа в .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Используйте объект SaveOptions, чтобы указать кодировку для документа, который мы будем сохранять.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// По умолчанию выходной документ .epub будет содержать всё своё содержимое в одной HTML‑части.
// Критерий разбиения позволяет разделить документ на несколько HTML‑частей.
// Мы установим критерий разбиения документа на абзацы заголовков.
// Это полезно для читателей, которые не могут открывать HTML‑файлы, превышающие определённый размер.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Укажите, что мы хотим экспортировать свойства документа.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
