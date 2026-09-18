---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter Methode"
linktitle: "get_SoftLineBreakCharacter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter Methode. Gibt einen Zeichenwert zurück oder setzt ihn, der einen weichen Zeilenumbruch darstellt. Der Standardwert ist SPACE (U+0020) in C++."
type: docs
weight: 4500
url: /de/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


Liest oder setzt einen Zeichenwert, der **soft line break** darstellt. Der Standardwert ist **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## Beispiele



Zeigt, wie man das weiche Zeilenumbruchzeichen setzt.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## Siehe auch

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
