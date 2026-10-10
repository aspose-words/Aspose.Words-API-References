---
title: "Método Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter"
linktitle: "get_SoftLineBreakCharacter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter. Obtiene o establece un valor de carácter que representa un salto de línea suave. El valor predeterminado es SPACE (U+0020) en C++."
type: docs
weight: 4500
url: /es/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


Obtiene o establece un valor de carácter que representa **soft line break**. El valor predeterminado es **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## Ejemplos



Muestra cómo establecer el carácter de salto de línea suave.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## Ver también

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
