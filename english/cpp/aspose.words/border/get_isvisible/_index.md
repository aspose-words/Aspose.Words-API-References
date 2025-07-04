---
title: Aspose::Words::Border::get_IsVisible method
linktitle: get_IsVisible
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::get_IsVisible method. Returns true if the LineStyle is not None in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/border/get_isvisible/
---
## Border::get_IsVisible method


Returns **true** if the [LineStyle](../get_linestyle/) is not [None](../../linestyle/).

```cpp
bool Aspose::Words::Border::get_IsVisible()
```


## Examples



Shows how to remove borders from a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Each paragraph has an individual set of borders.
// We can access the settings for the appearance of these borders via the paragraph format object.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// We can remove a border at once by running the ClearFormatting method.
// Running this method on every border of a paragraph will remove all its borders.
for (auto&& border : System::IterateOver(borders))
{
    border->ClearFormatting();
}

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, borders->idx_get(0)->get_LineStyle());
ASSERT_FALSE(borders->idx_get(0)->get_IsVisible());

doc->Save(get_ArtifactsDir() + u"Border.ClearFormatting.docx");
```

## See Also

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
