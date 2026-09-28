---
title: "Метод Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter"
linktitle: "get_SoftLineBreakCharacter"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter. Получает или задает символьное значение, представляющее мягкий разрыв строки. Значение по умолчанию — SPACE (U+0020) в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


Получает или задает символьное значение, представляющее **мягкий разрыв строки**. Значение по умолчанию — **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## Примеры



Показывает, как установить символ мягкого разрыва строки.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## См. также

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
