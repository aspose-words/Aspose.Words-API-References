---
title: "Aspose::Words::ParagraphFormat::get_PageBreakBefore метод"
linktitle: "get_PageBreakBefore"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_PageBreakBefore метод. True если разрыв страницы принудительно вставлен перед абзацем в C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


Истина, если перед абзацем принудительно вставлен разрыв страницы.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## Примеры



Показывает, как создавать абзацы с разрывами страниц в начале.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите этот флаг в значение "true", чтобы применить разрыв страницы в начале каждого абзаца
// которые будет создавать построитель документа при этой конфигурации ParagraphFormat.
// Первый абзац не получит разрыв страницы.
// Оставьте этот флаг со значением "false", чтобы каждый новый абзац начинался на той же странице.
// как и ранее, при условии, что есть достаточно места.
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
