---
title: "Метод Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat. Указывает, включать ли текстовые поля, сноски и концевые сноски в статистику подсчёта слов в C++."
type: docs
weight: 33000
url: /ru/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


Указывает, включать ли текстовые поля, сноски и концевые сноски в статистику подсчёта слов.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## Примеры



Показывает, как включать или исключать текстовые поля, сноски и концевые сноски из статистики подсчёта слов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// По умолчанию параметр установлен в значение 'false'.
doc->UpdateWordCount();
// Подсчёт слов без текстовых полей, сносок и концевых сносок.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// Подсчёт слов с текстовыми полями, сносками и концевыми сносками.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
