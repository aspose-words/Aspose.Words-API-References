---
title: "Aspose::Words::DocumentBase::get_FootnoteSeparators метод"
linktitle: "get_FootnoteSeparators"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBase::get_FootnoteSeparators метод. Предоставляет доступ к разделителям сносок/конечных сносок, определённым в документе, в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


Обеспечивает доступ к разделителям сносок/концевых сносок, определённым в документе.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


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

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
