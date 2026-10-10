---
title: "Méthode Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields"
linktitle: "get_IgnoreFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields. Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs. La valeur par défaut est false en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefields/
---
## FindReplaceOptions::get_IgnoreFields method


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des champs. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields() const
```

## Remarques


Cette option affecte le champ entier (tous les nœuds entre [FieldStart](../../../aspose.words/nodetype/) et [FieldEnd](../../../aspose.words/nodetype/)).

Pour ignorer uniquement les codes de champ, veuillez utiliser l'option correspondante [IgnoreFieldCodes](../get_ignorefieldcodes/).

## Exemples



Montre comment ignorer le texte à l'intérieur des champs.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertField(u"QUOTE", u"Hello again!");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et remplacement.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Définissez le drapeau "IgnoreFields" sur "true" pour obtenir la recherche et remplacement
// opération afin d'ignorer le texte à l'intérieur des champs.
// Définissez le drapeau "IgnoreFields" sur "false" pour obtenir la recherche et remplacement
// opération afin de rechercher également le texte à l'intérieur des champs.
options->set_IgnoreFields(ignoreTextInsideFields);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideFields ? System::String(u"Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015") : System::String(u"Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015"), doc->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
