---
title: "Aspose::Words::Document::StopTrackRevisions method"
linktitle: "StopTrackRevisions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::StopTrackRevisions method. Останавливает автоматическое помечание изменений документа как ревизий в C++."
type: docs
weight: 93000
url: /ru/cpp/aspose.words/document/stoptrackrevisions/
---
## Document::StopTrackRevisions method


Останавливает автоматическое помечание изменений документа как ревизий.

```cpp
void Aspose::Words::Document::StopTrackRevisions()
```


## Примеры



Показывает, как отслеживать ревизии при редактировании документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Редактирование документа обычно не считается ревизией, пока мы не начнём их отслеживание.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// Прекратите отслеживание ревизий, чтобы будущие правки не учитывались как ревизии.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// Создание ревизий присваивает им дату и время операции.
// Мы можем отключить это, передавая DateTime.MinValue, когда начинаем отслеживать изменения.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// Мы можем принимать/отклонять эти изменения программно
// вызывая методы, такие как Document.AcceptAllRevisions, или метод Accept у каждой правки.
// В Microsoft Word мы можем обрабатывать их вручную через \"Review\" -> \"Changes\".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
