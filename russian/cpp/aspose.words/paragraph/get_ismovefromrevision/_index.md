---
title: "Aspose::Words::Paragraph::get_IsMoveFromRevision метод"
linktitle: "get_IsMoveFromRevision"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph::get_IsMoveFromRevision метод. Возвращает true, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words/paragraph/get_ismovefromrevision/
---
## Paragraph::get_IsMoveFromRevision method


Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений.

```cpp
bool Aspose::Words::Paragraph::get_IsMoveFromRevision()
```


## Примеры



Показывает, как проверить, является ли абзац перемещённой правкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Этот документ содержит правки «Move», которые появляются, когда мы выделяем текст курсором,
// а затем перетаскиваем его, чтобы переместить в другое место
// во время отслеживания правок в Microsoft Word через «Review» -> «Track changes».
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Правки перемещения состоят из пар правок «Move from» и «Move to».
// Эти правки являются потенциальными изменениями документа, которые мы можем принять или отклонить.
// Прежде чем принять/отклонить правку перемещения, документ
// должен отслеживать как исходные, так и конечные места текста.
// Второй и четвёртый абзацы определяют одну такую правку, поэтому оба имеют одинаковое содержание.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// Правка «Move from» — это абзац, из которого мы перетащили текст.
// Если мы примем правку, этот абзац исчезнет,
// а другой останется и больше не будет правкой.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// Правка «Move to» — это абзац, в который мы перетащили текст.
// Если мы отклоним правку, этот абзац исчезнет, а другой останется.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## См. также

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
