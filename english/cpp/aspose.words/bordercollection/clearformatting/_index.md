---
title: Aspose::Words::BorderCollection::ClearFormatting method
linktitle: ClearFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection::ClearFormatting method. Removes all borders of an object in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


Removes all borders of an object.

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## Examples



Shows how to remove all borders from all paragraphs in a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// The first paragraph of this document has visible borders with these settings.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// Use the "ClearFormatting" method on each paragraph to remove all borders.
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

## See Also

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
