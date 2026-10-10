---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter metodo"
linktitle: "get_SoftLineBreakCharacter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter metodo. Ottiene o imposta un valore di carattere che rappresenta l'interruzione di riga morbida. Il valore predefinito è SPACE (U+0020) in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


Ottiene o imposta un valore di carattere che rappresenta **soft line break**. Il valore predefinito è **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## Esempi



Mostra come impostare il carattere di interruzione di riga morbida.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## Vedi anche

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
