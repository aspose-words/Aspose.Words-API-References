---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted méthode"
linktitle: "get_IgnoreInserted"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted méthode. Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions d'insertion. La valeur par défaut est false en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreinserted/
---
## FindReplaceOptions::get_IgnoreInserted method


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions d'insertion. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted() const
```


## Exemples



Montre comment inclure ou ignorer le texte à l'intérieur des révisions d'insertion lors d'une opération de recherche et remplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// Commencez à suivre les révisions et insérez un paragraphe. Ce paragraphe sera une révision d'insertion.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "IgnoreInserted" sur "true" pour obtenir la recherche et remplacement
// opération afin d'ignorer les paragraphes qui sont des révisions d'insertion.
// Définissez le drapeau "IgnoreInserted" sur "false" pour obtenir la recherche et remplacement
// opération afin de rechercher également le texte à l'intérieur des révisions d'insertion.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
