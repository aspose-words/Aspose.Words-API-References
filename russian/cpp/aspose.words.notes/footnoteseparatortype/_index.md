---
title: "Aspose::Words::Notes::FootnoteSeparatorType enum"
linktitle: "FootnoteSeparatorType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::FootnoteSeparatorType enum. Указывает тип разделителя сноски/концевой сноски в C++."
type: docs
weight: 6500
url: /ru/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


Указывает тип разделителя сноски/концевой сноски.

```cpp
enum class FootnoteSeparatorType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| FootnoteSeparator | 0 | Разделитель между основным текстом и текстом сноски. |
| FootnoteContinuationSeparator | 1 | Печатается над текстом сноски на странице, когда текст должен быть продолжен с предыдущей страницы. |
| FootnoteContinuationNotice | 2 | Печатается под текстом сноски на странице, когда текст сноски должен быть продолжен на следующей странице. |
| EndnoteSeparator | 3 | Разделитель между основным текстом и текстом концевой сноски. |
| EndnoteContinuationSeparator | 4 | Печатается над текстом концевой сноски на странице, когда текст должен быть продолжен с предыдущей страницы. |
| EndnoteContinuationNotice | 5 | Печатается под текстом концевой сноски на странице, когда текст концевой сноски должен быть продолжен на следующей странице. |


## Примеры



Показывает, как удалить разделитель концевой сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Удалить разделитель концевой сноски.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


Показывает, как управлять форматом разделителя сносок.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Выровнять разделитель сносок.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## См. также

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
