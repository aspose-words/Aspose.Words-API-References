---
title: "Classe Aspose::Words::Fields::UserInformation"
linktitle: "UserInformation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Fields::UserInformation. Spécifie les informations sur l'utilisateur. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 117000
url: /fr/cpp/aspose.words.fields/userinformation/
---
## UserInformation class


Spécifie les informations sur l'utilisateur. Pour en savoir plus, visitez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class UserInformation : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Address](./get_address/)() const | Obtient ou définit l'adresse postale de l'utilisateur. |
| static [get_DefaultUser](./get_defaultuser/)() | Informations utilisateur par défaut. |
| [get_Initials](./get_initials/)() const | Obtient ou définit les initiales de l'utilisateur. |
| [get_Name](./get_name/)() const | Obtient ou définit le nom de l'utilisateur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Address](./set_address/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::UserInformation::get_Address](./get_address/). |
| [set_Initials](./set_initials/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::UserInformation::get_Initials](./get_initials/). |
| [set_Name](./set_name/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::UserInformation::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [UserInformation](./userinformation/)() |  |

## Exemples



Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un objet UserInformation et définissez-le comme source de données pour les champs qui affichent les informations de l'utilisateur.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Insérez les champs USERNAME, USERINITIALS et USERADDRESS, qui affichent les valeurs de
// les propriétés respectives de l'objet UserInformation que nous avons créé ci-dessus.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// L'objet d'options de champ possède également un utilisateur par défaut statique auquel les champs de tous les documents peuvent se référer.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
