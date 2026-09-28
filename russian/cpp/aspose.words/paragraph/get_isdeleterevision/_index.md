---
title: "Aspose::Words::Paragraph::get_IsDeleteRevision метод"
linktitle: "get_IsDeleteRevision"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph::get_IsDeleteRevision метод. Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/paragraph/get_isdeleterevision/
---
## Paragraph::get_IsDeleteRevision method


Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений.

```cpp
bool Aspose::Words::Paragraph::get_IsDeleteRevision()
```


## Примеры



Показывает, как работать с абзацами‑ревизиями.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// Вышеуказанные абзацы не являются ревизиями.
// Абзацы, которые мы добавляем после начала отслеживания изменений, будут зарегистрированы как ревизии "Insert".
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// Абзацы, которые мы удаляем после начала отслеживания изменений, будут зарегистрированы как ревизии "Delete".
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// Такие абзацы останутся, пока мы не примем или не отклоним ревизию удаления.
// Принятие ревизии окончательно удалит абзац,
// а отклонение ревизии оставит его в документе, как будто мы его никогда не удаляли.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// Примите ревизию, а затем убедитесь, что абзац исчез.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## См. также

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
