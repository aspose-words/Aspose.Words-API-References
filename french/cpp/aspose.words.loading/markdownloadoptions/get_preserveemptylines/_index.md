---
title: "Méthode Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines"
linktitle: "get_PreserveEmptyLines"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines. Obtient ou définit une valeur booléenne indiquant s'il faut préserver les lignes vides lors du chargement d'un document Markdown. La valeur par défaut est false. Normalement, les lignes vides entre les éléments de niveau bloc dans Markdown sont ignorées. Les lignes vides au début et à la fin du document sont également ignorées. Cette option permet d'importer ces lignes vides en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


Obtient ou définit une valeur booléenne indiquant s'il faut préserver les lignes vides lors du chargement d'un document [Markdown](../../../aspose.words/loadformat/). La valeur par défaut est **false**. Normalement, les lignes vides entre les éléments de niveau bloc dans Markdown sont ignorées. Les lignes vides au début et à la fin du document sont également ignorées. Cette option permet d'importer ces lignes vides.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
```


## Exemples



Montre comment préserver les lignes vides lors du chargement d'un document.
```cpp
System::String mdText = System::String::Format(u"{0}Line1{1}{2}Line2{3}{4}", System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine());
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(mdText));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_PreserveEmptyLines(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"\rLine1\r\rLine2\r\f", doc->GetText());
}
```

## Voir aussi

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
