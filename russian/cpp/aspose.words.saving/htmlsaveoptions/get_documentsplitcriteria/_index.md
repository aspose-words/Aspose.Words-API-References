---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria метод"
linktitle: "get_DocumentSplitCriteria"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria метод. Указывает, как документ должен быть разделён при сохранении в формат Html, Epub или Azw3. По умолчанию None для HTML и HeadingParagraph для EPUB и AZW3 в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


Указывает, как документ должен быть разделён при сохранении в формат [Html](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/) или [Azw3](../../../aspose.words/saveformat/). По умолчанию [None](../../documentsplitcriteria/) для HTML и [HeadingParagraph](../../documentsplitcriteria/) для EPUB и AZW3.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## Примечания


Обычно вы хотите, чтобы документ сохранялся в HTML как один файл. Но в некоторых случаях предпочтительнее разбить вывод на несколько более мелких HTML‑страниц. При сохранении в формате HTML эти страницы будут выводиться в отдельные файлы или потоки. При сохранении в формате EPUB они будут включены в соответствующие пакеты.

Документ нельзя разбивать при сохранении в формате MHTML.

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

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
