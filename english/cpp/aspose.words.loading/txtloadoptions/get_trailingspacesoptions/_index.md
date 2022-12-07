---
title: get_TrailingSpacesOptions
second_title: Aspose.Words for C++ API Reference
description: Gets or sets preferred option of a trailing space handling. Default value is Trim.
type: docs
weight: 79
url: /cpp/aspose.words.loading/txtloadoptions/get_trailingspacesoptions/
---
## TxtLoadOptions::get_TrailingSpacesOptions method


Gets or sets preferred option of a trailing space handling. Default value is [Trim](../../txttrailingspacesoptions/).

```cpp
Aspose::Words::Loading::TxtTrailingSpacesOptions Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions() const
```


## Examples



Shows how to trim whitespace when loading plaintext documents. 
```cpp
String textDoc = String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
auto loadOptions = MakeObject<TxtLoadOptions>();

// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
// to preserve all whitespace characters at the start of every line.
// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
// to remove all whitespace characters from the start of every line,
// and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
// to remove all whitespace characters from every line's start.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
// to preserve all whitespace characters at the end of every line.
// Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
// remove all whitespace characters from the end of every line.
loadOptions->set_TrailingSpacesOptions(txtTrailingSpacesOptions);

auto doc = MakeObject<Document>(MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);
SharedPtr<ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

switch (txtLeadingSpacesOptions)
{
case TxtLeadingSpacesOptions::ConvertToIndent:
    ASPOSE_ASSERT_EQ(37.8, paragraphs->idx_get(0)->get_ParagraphFormat()->get_FirstLineIndent());
    ASPOSE_ASSERT_EQ(25.2, paragraphs->idx_get(1)->get_ParagraphFormat()->get_FirstLineIndent());
    ASPOSE_ASSERT_EQ(6.3, paragraphs->idx_get(2)->get_ParagraphFormat()->get_FirstLineIndent());
    ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
    ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
    ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
    break;

case TxtLeadingSpacesOptions::Preserve:
    ASSERT_TRUE(paragraphs->LINQ_All([](SharedPtr<Node> p)
                                     { return (System::DynamicCast<Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0; }));
    ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"      Line 1"));
    ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"    Line 2"));
    ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u" Line 3"));
    break;

case TxtLeadingSpacesOptions::Trim:
    ASSERT_TRUE(paragraphs->LINQ_All([](SharedPtr<Node> p)
                                     { return (System::DynamicCast<Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0; }));
    ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
    ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
    ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
    break;
}

switch (txtTrailingSpacesOptions)
{
case TxtTrailingSpacesOptions::Preserve:
    ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1 \r"));
    ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2   \r"));
    ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3       \f"));
    break;

case TxtTrailingSpacesOptions::Trim:
    ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1\r"));
    ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2\r"));
    ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3\f"));
    break;
}
```

## See Also

* Enum [TxtTrailingSpacesOptions](../../txttrailingspacesoptions/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
