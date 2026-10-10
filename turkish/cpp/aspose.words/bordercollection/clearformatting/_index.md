---
title: "Aspose::Words::BorderCollection::ClearFormatting yöntemi"
linktitle: "ClearFormatting"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::ClearFormatting yöntemi. C++'da bir nesnenin tüm kenarlarını kaldırır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


Bir nesnenin tüm kenarlarını kaldırır.

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## Örnekler



Bir belgedeki tüm paragraflardan tüm kenarları nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Bu belgenin ilk paragrafı, bu ayarlarla görünür kenarlara sahiptir.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// "ClearFormatting" yöntemini her paragrafta kullanarak tüm kenarları kaldırın.
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

## Ayrıca Bakınız

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
