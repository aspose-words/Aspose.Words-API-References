---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter metodu"
linktitle: "get_SoftLineBreakCharacter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter metodu. Yumuşak satır sonunu temsil eden bir karakter değerini alır veya ayarlar. Varsayılan değer C++'ta SPACE (U+0020)'dır."
type: docs
weight: 4500
url: /tr/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


**soft line break**'i temsil eden bir karakter değerini alır veya ayarlar. Varsayılan değer **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## Örnekler



Yumuşak satır sonu karakterinin nasıl ayarlanacağını gösterir.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## Ayrıca Bakınız

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
