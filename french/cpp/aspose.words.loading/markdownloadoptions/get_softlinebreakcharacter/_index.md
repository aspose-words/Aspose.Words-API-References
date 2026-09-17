---
title: "Méthode Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter"
linktitle: "get_SoftLineBreakCharacter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter. Obtient ou définit une valeur de caractère représentant un saut de ligne doux. La valeur par défaut est SPACE (U+0020) en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


Obtient ou définit une valeur de caractère représentant **soft line break**. La valeur par défaut est **SPACE (U+0020)**.

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## Exemples



Montre comment définir le caractère de saut de ligne doux.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## Voir aussi

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
