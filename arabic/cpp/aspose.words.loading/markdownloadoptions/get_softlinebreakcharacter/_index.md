---
title: "طريقة Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter"
linktitle: "get_SoftLineBreakCharacter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter. يحصل أو يضبط قيمة حرفية تمثل فاصل سطر ناعم. القيمة الافتراضية هي SPACE (U+0020) في C++."
type: docs
weight: 4500
url: /ar/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


يحصل أو يعيّن قيمة حرفية تمثل **soft line break**. القيمة الافتراضية هي **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## أمثلة



يعرض كيفية تعيين حرف فاصل سطر ناعم.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## انظر أيضًا

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
