---
title: "Méthode Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted"
linktitle: "get_IgnoreDeleted"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted. Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est false en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des révisions de suppression. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## Exemples



Montre comment inclure ou ignorer le texte à l'intérieur des révisions de suppression lors d'une opération de recherche et remplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Commencez à suivre les révisions et supprimez le deuxième paragraphe, ce qui créera une révision de suppression.
// Ce paragraphe restera dans le document jusqu'à ce que nous acceptions la révision de suppression.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "IgnoreDeleted" sur "true" pour obtenir la recherche et remplacement
// opération afin d'ignorer les paragraphes qui sont des révisions de suppression.
// Définissez le drapeau "IgnoreDeleted" sur "false" pour obtenir la recherche et remplacement
// opération afin de rechercher également le texte à l'intérieur des révisions de suppression.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
