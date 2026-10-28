---
title: Aspose::Words::Loading::MarkdownLoadOptions::set_SoftLineBreakCharacter method
linktitle: set_SoftLineBreakCharacter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::MarkdownLoadOptions::set_SoftLineBreakCharacter method. Sets a character value representing `soft line break`. The default value is SPACE (U+0020) in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.loading/markdownloadoptions/set_softlinebreakcharacter/
---
## MarkdownLoadOptions::set_SoftLineBreakCharacter method


Sets a character value representing `soft line break`. The default value is **SPACE (U+0020)**.

```cpp
void Aspose::Words::Loading::MarkdownLoadOptions::set_SoftLineBreakCharacter(char16_t value)
```

## Remarks

 Note, setting this option to [LineBreakChar](../../../aspose.words/controlchar/linebreakchar/) allows you to load soft line breaks as hard line breaks. 
## Examples


Shows how to set soft line break character.

```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```
## See Also

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
