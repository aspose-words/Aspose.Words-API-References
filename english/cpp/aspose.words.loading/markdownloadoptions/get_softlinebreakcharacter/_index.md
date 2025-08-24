---
title: Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter method
linktitle: get_SoftLineBreakCharacter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter method. Gets or sets a character value representing soft line break. The default value is SPACE (U+0020) in C++.'
type: docs
weight: 4500
url: /cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


Gets or sets a character value representing **soft line break**. The default value is **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## Examples



Shows how to set soft line break character. 
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## See Also

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
