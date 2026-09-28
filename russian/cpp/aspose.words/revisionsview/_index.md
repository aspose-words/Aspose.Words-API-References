---
title: "Перечисление Aspose::Words::RevisionsView"
linktitle: "RevisionsView"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::RevisionsView. Позволяет указать, работать ли с оригинальной или исправленной версией документа в C++."
type: docs
weight: 112000
url: /ru/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


Позволяет указать, работать ли с оригинальной или исправленной версией документа.

```cpp
enum class RevisionsView
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Original | 0 | Указывает оригинальную версию документа. |
| Final | 1 | Указывает исправленную версию документа. |


## Примеры



Показывает, как переключаться между исправленным и оригинальным представлением документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// Просмотр объекта документа так, как если бы все исправления были приняты. В настоящее время поддерживает метки списков.
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
