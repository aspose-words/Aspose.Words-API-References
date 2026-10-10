---
title: "Méthode get_UserName de Aspose::Words::Fields::FieldUserName"
linktitle: "get_UserName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldUserName::get_UserName method. Obtient ou définit le nom de l'utilisateur actuel en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


Obtient ou définit le nom de l'utilisateur actuel.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## Exemples



Montre comment utiliser le champ USERNAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez un objet UserInformation et définissez-le comme source d'informations utilisateur pour tous les champs que nous créons.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un champ USERNAME pour afficher le nom de l'utilisateur actuel,
// extrait de l'objet UserInformation que nous avons créé ci-dessus.
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// Nous pouvons définir cette propriété pour que notre champ remplace la valeur actuellement stockée dans l'objet UserInformation.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// Cela n'affecte pas la valeur dans l'objet UserInformation.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## Voir aussi

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
