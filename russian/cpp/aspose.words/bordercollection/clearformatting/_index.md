---
title: "Метод Aspose::Words::BorderCollection::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::BorderCollection::ClearFormatting. Удаляет все границы объекта в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


Удаляет все границы объекта.

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## Примеры



Показано, как удалить все границы из всех абзацев в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Первый абзац этого документа имеет видимые границы с этими настройками.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// Используйте метод "ClearFormatting" для каждого абзаца, чтобы удалить все границы.
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    paragraph->get_ParagraphFormat()->get_Borders()->ClearFormatting();

    for (auto&& border : System::IterateOver(paragraph->get_ParagraphFormat()->get_Borders()))
    {
        ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
        ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());
        ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
    }
}

doc->Save(get_ArtifactsDir() + u"BorderCollection.RemoveAllBorders.docx");
```

## См. также

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
