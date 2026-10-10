---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes method"
linktitle: "get_IgnoreFieldCodes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes method. Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ. La valeur par défaut est false en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefieldcodes/
---
## FindReplaceOptions::get_IgnoreFieldCodes method


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur des codes de champ. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes() const
```

## Remarques


Cette option affecte uniquement les codes de champ (elle n'ignore pas les nœuds entre [FieldSeparator](../../../aspose.words/nodetype/) et [FieldEnd](../../../aspose.words/nodetype/)).

Pour ignorer le champ entier, veuillez utiliser l'option correspondante [IgnoreFields](../get_ignorefields/).

## Exemples



Montre comment ignorer le texte à l'intérieur des codes de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u"INCLUDETEXT", u"Test IT!");

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFieldCodes(ignoreFieldCodes);

// Remplacez 'T' dans le document en ignorant le texte à l'intérieur du code de champ ou non.
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"T"), u"*", options);
std::cout << doc->GetText() << std::endl;

ASSERT_EQ(ignoreFieldCodes ? System::String(u"\u0013INCLUDETEXT\u0014*est I*!\u0015") : System::String(u"\u0013INCLUDE*EX*\u0014*est I*!\u0015"), doc->GetText().Trim());
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
