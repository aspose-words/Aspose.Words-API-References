---
title: "Метод Aspose::Words::Story::get_Paragraphs"
linktitle: "get_Paragraphs"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Story::get_Paragraphs. Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/story/get_paragraphs/
---
## Story::get_Paragraphs method


Возвращает коллекцию абзацев, которые являются непосредственными дочерними элементами истории.

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::Story::get_Paragraphs() override
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

* Class [ParagraphCollection](../../paragraphcollection/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
