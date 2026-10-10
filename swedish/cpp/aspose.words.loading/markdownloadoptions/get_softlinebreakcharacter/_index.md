---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter‑metod"
linktitle: "get_SoftLineBreakCharacter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter‑metod. Hämtar eller anger ett teckenvärde som representerar mjukt radbryt. Standardvärdet är SPACE (U+0020) i C++."
type: docs
weight: 4500
url: /sv/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


Hämtar eller anger ett teckenvärde som representerar **soft line break**. Standardvärdet är **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## Exempel



Visar hur man anger tecknet för mjukt radbryt.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## Se även

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
