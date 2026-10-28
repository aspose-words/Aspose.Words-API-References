---
title: Aspose::Words::Loading::MarkdownLoadOptions::set_ImportUnderlineFormatting method
linktitle: set_ImportUnderlineFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::MarkdownLoadOptions::set_ImportUnderlineFormatting method. Sets a boolean value indicating either to recognize a sequence of two plus characters "++" as underline text formatting. The default value is false in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.loading/markdownloadoptions/set_importunderlineformatting/
---
## MarkdownLoadOptions::set_ImportUnderlineFormatting method


Sets a boolean value indicating either to recognize a sequence of two plus characters "++" as underline text formatting. The default value is **false**.

```cpp
void Aspose::Words::Loading::MarkdownLoadOptions::set_ImportUnderlineFormatting(bool value)
```

## Examples


Shows how to recognize plus characters "++" as underline text formatting.

```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_ASCII()->GetBytes(u"++12 and B++"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_ImportUnderlineFormatting(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));
    ASSERT_EQ(Underline::Single, para->get_Runs()->idx_get(0)->get_Font()->get_Underline());

    loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_ImportUnderlineFormatting(false);
    doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));
    ASSERT_EQ(Underline::None, para->get_Runs()->idx_get(0)->get_Font()->get_Underline());
}
```
## See Also

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
