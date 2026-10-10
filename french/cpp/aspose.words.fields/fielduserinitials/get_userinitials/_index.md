---
title: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials méthode"
linktitle: "get_UserInitials"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials méthode. Obtient ou définit les initiales de l'utilisateur actuel en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


Obtient ou définit les initiales de l'utilisateur actuel.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## Exemples



Montre comment utiliser le champ USERINITIALS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez un objet UserInformation et définissez-le comme source d'informations utilisateur pour tous les champs que nous créons.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Créez un champ USERINITIALS pour afficher les initiales de l'utilisateur actuel,
// extrait de l'objet UserInformation que nous avons créé ci-dessus.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// Nous pouvons définir cette propriété pour que notre champ remplace la valeur actuellement stockée dans l'objet UserInformation.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// Cela n'affecte pas la valeur dans l'objet UserInformation.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## Voir aussi

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
