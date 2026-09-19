---
title: "Aspose::Words::Fields::UserInformation classe"
linktitle: "UserInformation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::UserInformation classe. Specifica le informazioni sull'utente. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 117000
url: /it/cpp/aspose.words.fields/userinformation/
---
## UserInformation class


Specifica informazioni sull'utente. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class UserInformation : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Address](./get_address/)() const | Ottiene o imposta l'indirizzo postale dell'utente. |
| static [get_DefaultUser](./get_defaultuser/)() | Informazioni utente predefinite. |
| [get_Initials](./get_initials/)() const | Ottiene o imposta le iniziali dell'utente. |
| [get_Name](./get_name/)() const | Ottiene o imposta il nome dell'utente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Address](./set_address/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::UserInformation::get_Address](./get_address/). |
| [set_Initials](./set_initials/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::UserInformation::get_Initials](./get_initials/). |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::UserInformation::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [UserInformation](./userinformation/)() |  |

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
