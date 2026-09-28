---
title: "Aspose::Words::Saving::DocumentSplitCriteria enum"
linktitle: "DocumentSplitCriteria"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::DocumentSplitCriteria enum. Указывает, как документ разбивается на части при сохранении в формат Html, Epub или Azw3 в C++."
type: docs
weight: 52000
url: /ru/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


Указывает, как документ разбивается на части при сохранении в формат [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) или [Azw3](../../aspose.words/saveformat/).

```cpp
enum class DocumentSplitCriteria
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Документ не разбивается. |
| PageBreak | 1 | Документ разбивается на части в явных разрывах страниц. Разрыв страницы может быть задан символом [PageBreak](../../aspose.words/controlchar/pagebreak/), разрывом раздела, указывающим начало нового раздела на новой странице, или абзацем, у которого свойство [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) установлено в **true**. |
| ColumnBreak | 2 | Документ разбивается на части в разрывах колонок. Разрыв колонки может быть задан символом [ColumnBreak](../../aspose.words/controlchar/columnbreak/) или разрывом раздела, указывающим начало нового раздела в новой колонке. |
| SectionBreak | 4 | Документ разбивается на части при разрыве раздела любого типа. |
| HeadingParagraph | 8 | Документ разбивается на части в абзаце, отформатированном с использованием стиля заголовка **Heading 1**, **Heading 2** и т.д. Используйте совместно с [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/), чтобы указать уровни заголовков (от 1 до указанного уровня), при которых происходит разбиение. |

## Примечания


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Разные критерии могут частично перекрываться. Например, стиль **Heading 1** часто имеет свойство [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/), поэтому он подпадает под два критерия: [PageBreak](./) и [HeadingParagraph](./). Некоторые разрывы разделов могут вызывать разрывы страниц и т.д. В типичных случаях указание только одного флага является наиболее практичным вариантом.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
