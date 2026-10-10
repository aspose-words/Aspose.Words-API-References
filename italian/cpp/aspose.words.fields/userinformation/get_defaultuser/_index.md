---
title: "Aspose::Words::Fields::UserInformation::get_DefaultUser metodo"
linktitle: "get_DefaultUser"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::UserInformation::get_DefaultUser metodo. Informazioni sull'utente predefinito in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.fields/userinformation/get_defaultuser/
---
## UserInformation::get_DefaultUser method


Informazioni utente predefinite.

```cpp
static System::SharedPtr<Aspose::Words::Fields::UserInformation> Aspose::Words::Fields::UserInformation::get_DefaultUser()
```


## Esempi



Mostra come impostare i dettagli dell'utente e visualizzarli usando i campi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un oggetto UserInformation e impostalo come origine dati per i campi che visualizzano le informazioni dell'utente.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Inserisci i campi USERNAME, USERINITIALS e USERADDRESS, che visualizzano i valori di
// le rispettive proprietà dell'oggetto UserInformation che abbiamo creato sopra.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// L'oggetto field options ha anche un utente predefinito statico a cui i campi di tutti i documenti possono fare riferimento.
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

## Vedi anche

* Class [UserInformation](../)
* Class [UserInformation](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
