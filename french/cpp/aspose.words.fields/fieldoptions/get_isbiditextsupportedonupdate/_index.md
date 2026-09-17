---
title: "Méthode Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate. Obtient ou définit la valeur indiquant si le texte bidirectionnel est entièrement pris en charge lors de la mise à jour du champ ou non en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


Obtient ou définit la valeur indiquant si le texte bidirectionnel est entièrement pris en charge lors de la mise à jour du champ ou non.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## Remarques


Lorsque cette propriété est définie sur **true**, des étapes supplémentaires sont effectuées pour produire un résultat de champ compatible avec les langues de droite à gauche (c.-à-d. l'arabe ou l'hébreu) lors de sa mise à jour.

Lorsque cette propriété est définie sur **false** et qu'une langue de droite à gauche est utilisée, la justesse du résultat du champ après sa mise à jour n'est pas garantie.

La valeur par défaut est **false**.

## Exemples



Montre comment utiliser [FieldOptions](../) pour garantir que la mise à jour des champs prend pleinement en charge le texte bidirectionnel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Assurez-vous que toute opération de champ impliquant du texte de droite à gauche s'exécute comme prévu.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Utilisez un constructeur de document pour insérer un champ contenant le texte de droite à gauche.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## Voir aussi

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
