---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress méthode"
linktitle: "get_UserAddress"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress méthode. Obtient ou définit l'adresse postale de l'utilisateur actuel en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


Obtient ou définit l'adresse postale de l'utilisateur actuel.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## Exemples



Montre comment utiliser le champ USERADDRESS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez un objet UserInformation et définissez-le comme source d'informations utilisateur pour tous les champs que nous créons.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Créez un champ USERADDRESS pour afficher l'adresse de l'utilisateur actuel,
// extrait de l'objet UserInformation que nous avons créé ci-dessus.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// Nous pouvons définir cette propriété pour que notre champ remplace la valeur actuellement stockée dans l'objet UserInformation.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// Cela n'affecte pas la valeur dans l'objet UserInformation.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## Voir aussi

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
