---
title: "Aspose::Words::Document::StartTrackRevisions метод"
linktitle: "StartTrackRevisions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::StartTrackRevisions метод. Автоматически начинает помечать все последующие изменения, внесённые в документ программно, как изменения ревизий в C++."
type: docs
weight: 92000
url: /ru/cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


Автоматически начинает помечать все последующие изменения, которые вы вносите в документ программно, как изменения ревизий.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
## Примечания


Если вы вызовете этот метод, а затем внесёте изменения в документ программно, сохраните документ и позже откроете его в MS Word, вы увидите эти изменения как правки.

В настоящее время Aspose.Words поддерживает отслеживание только вставок и удалений узлов. Изменения форматирования не фиксируются как правки.

Автоматическое отслеживание изменений поддерживается как при модификации этого документа через манипуляции узлами, так и при использовании [DocumentBuilder](../../documentbuilder/)

Этот метод не изменяет параметр [TrackRevisions](../get_trackrevisions/) и не использует его значение для отслеживания правок.

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
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


Автоматически начинает помечать все последующие изменения, которые вы вносите в документ программно, как изменения ревизий.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
## Примечания


Если вы вызовете этот метод, а затем внесёте изменения в документ программно, сохраните документ и позже откроете его в MS Word, вы увидите эти изменения как правки.

В настоящее время Aspose.Words поддерживает отслеживание только вставок и удалений узлов. Изменения форматирования не фиксируются как правки.

Автоматическое отслеживание изменений поддерживается как при модификации этого документа через манипуляции узлами, так и при использовании [DocumentBuilder](../../documentbuilder/)

Этот метод не изменяет параметр [TrackRevisions](../get_trackrevisions/) и не использует его значение для отслеживания правок.

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
