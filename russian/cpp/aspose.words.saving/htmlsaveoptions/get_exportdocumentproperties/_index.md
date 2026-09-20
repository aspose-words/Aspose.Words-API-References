---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties метод"
linktitle: "get_ExportDocumentProperties"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties метод. Указывает, следует ли экспортировать встроенные и пользовательские свойства документа в HTML, MHTML или EPUB. Значение по умолчанию — false в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportdocumentproperties/
---
## HtmlSaveOptions::get_ExportDocumentProperties method


Указывает, следует ли экспортировать встроенные и пользовательские свойства документа в HTML, MHTML или EPUB. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties() const
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

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
