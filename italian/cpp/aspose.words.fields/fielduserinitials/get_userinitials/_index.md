---
title: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials metodo"
linktitle: "get_UserInitials"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials metodo. Ottiene o imposta le iniziali dell'utente corrente in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


Ottiene o imposta le iniziali dell'utente corrente.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## Esempi



Mostra come utilizzare il campo USERINITIALS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un oggetto UserInformation e impostalo come origine delle informazioni utente per tutti i campi che creiamo.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Crea un campo USERINITIALS per visualizzare le iniziali dell'utente corrente,
// preso dall'oggetto UserInformation che abbiamo creato sopra.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// Possiamo impostare questa proprietà per far sì che il nostro campo sovrascriva il valore attualmente memorizzato nell'oggetto UserInformation.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// Questo non influisce sul valore nell'oggetto UserInformation.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## Vedi anche

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
