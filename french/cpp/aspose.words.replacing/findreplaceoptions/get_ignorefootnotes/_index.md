---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes méthode"
linktitle: "get_IgnoreFootnotes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes. Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les notes de bas de page. La valeur par défaut est false en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer les notes de bas de page. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## Exemples



Montre comment ignorer les notes de bas de page lors d'une opération de recherche et remplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Définissez le drapeau "IgnoreFootnotes" sur "true" pour obtenir la recherche et remplacement
// opération afin d'ignorer le texte à l'intérieur des notes de bas de page.
// Définissez le drapeau "IgnoreFootnotes" sur "false" pour obtenir la recherche et remplacement
// opération afin de rechercher également le texte à l'intérieur des notes de bas de page.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
