---
title: "Метод Aspose::Words::InlineStory::get_IsInsertRevision"
linktitle: "get_IsInsertRevision"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::InlineStory::get_IsInsertRevision. Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/inlinestory/get_isinsertrevision/
---
## InlineStory::get_IsInsertRevision method


Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений.

```cpp
bool Aspose::Words::InlineStory::get_IsInsertRevision()
```


## Примеры



Показывает, как просматривать свойства, связанные с изменениями, узлов [InlineStory](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision footnotes.docx");

// Когда мы редактируем документ при включённой опции "Track Changes", доступной через Review -> Tracking,
// в Microsoft Word, внесённые нами изменения считаются ревизиями.
// При редактировании документа с использованием Aspose.Words мы можем начать отслеживание ревизий, вызвав
// вызывая метод документа "StartTrackRevisions" и прекращая отслеживание с помощью метода "StopTrackRevisions".
// Мы можем либо принять ревизии, чтобы включить их в документ
// или отклонить их, чтобы отменить и избавиться от предложенного изменения.
ASSERT_TRUE(doc->get_HasRevisions());

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Notes::Footnote>>> footnotes = doc->GetChildNodes(Aspose::Words::NodeType::Footnote, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Notes::Footnote> >()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// Ниже перечислены пять типов правок, которые могут пометить узел InlineStory.
// 1 -  Вставка "insert" ревизии:
// Эта ревизия происходит, когда мы вставляем текст при отслеживании изменений.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  Правка "перемещение из":
// Когда мы выделяем текст в Microsoft Word и затем перетаскиваем его в другое место в документе
// при отслеживании изменений появляются две ревизии.
// Ревизия "move from" является копией исходного текста до его перемещения.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  Правка "перемещение в":
// Ревизия "move to" — это текст, который мы переместили в новое положение в документе.
// Ревизии "Move from" и "move to" появляются парами для каждой выполненной нами ревизии перемещения.
// Принятие ревизии перемещения удаляет ревизию "move from" и её текст,
// и сохраняет текст из ревизии "move to".
// Отклонение ревизии перемещения, наоборот, сохраняет ревизию "move from" и удаляет ревизию "move to".
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  Правка "удаление":
// Эта ревизия происходит, когда мы удаляем текст при отслеживании изменений. Когда мы удаляем текст таким образом,
// он останется в документе как ревизия, пока мы не примем её,
// что навсегда удалит текст, или отклонит ревизию, что сохранит удалённый текст на месте.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## См. также

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
